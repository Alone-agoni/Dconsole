## 简介

DConsole 是一个免费开源的，快速、简单的Thinkphp3.2命令行工具，使用DConsole可以快速生成ThinkPHP3.2框架中的controller，model，view

## 特性支持

最新的DConsole为WEB应用开发提供了以下支持：

*  一步生成controller、model、view
*  单独生成controller、model、view
*  自定义模板内容

命令：

*  php console generate:c 生成controller
*  php console generate:m 生成model
*  php console generate:v 生成view

### 如何使用Dconsole

将Dconsole下载后放在项目同级位置

### 如何使用Console一步生成功能

1、配置

```
$config = array(
	'PROCECT_NAME' => 'Cms', //项目名称
	'APP_NAME'     => 'Application', //应用名称
	'GENERATE_ALL' => true	//是否开启一步生成功能
);
```

2、命令

```
wei@wei:~/share/Console$ php console generate:c
Please enter the controller name :demo/article
> File is generated success!	../Cms/Application/Demo/Controller/ArticleController.class.php
> File is generated success!	../Cms/Application/Demo/Model/ArticleModel.class.php
> File is generated success!	../Cms/Application/Demo/View/Article/index.html
> File is generated success!	../Cms/Application/Demo/View/Article/create.html
> File is generated success!	../Cms/Application/Demo/View/Article/edit.html
wei@wei:~/share/Console$
```

### 如何使用Console单独生成功能

1、配置

```
$config = array(
	'PROCECT_NAME' => 'Cms', //项目名称
	'APP_NAME'     => 'Application', //应用名称
	'GENERATE_ALL' => false	//是否开启一步生成功能
);
```

2、命令

```
wei@wei:~/share/Console$ php console generate:c
Please enter the controller name :demo/article
> File is generated success!	../Cms/Application/Demo/Controller/ArticleController.class.php
wei@wei:~/share/Console$ php console generate:m
Please enter the model name :demo/article
> File is generated success!	../Cms/Application/Demo/Model/ArticleModel.class.php
wei@wei:~/share/Console$ php console generate:v
Please enter the view name :demo/article/index
> File is generated success!	../Cms/Application/Demo/View/Article/index.html
wei@wei:~/share/Console$
```

注意：就算开启了一步生成功能，也可以单独生成model、view

```
wei@wei:~/share/Console$ php console generate:c
Please enter the controller name :demo/article
> File is generated success!	../Cms/Application/Demo/Controller/ArticleController.class.php
> File is generated success!	../Cms/Application/Demo/Model/ArticleModel.class.php
> File is generated success!	../Cms/Application/Demo/View/Article/index.html
> File is generated success!	../Cms/Application/Demo/View/Article/create.html
> File is generated success!	../Cms/Application/Demo/View/Article/edit.html
wei@wei:~/share/Console$ php console generate:m
Please enter the model name :demo/category
> File is generated success!	../Cms/Application/Demo/Model/CategoryModel.class.php
wei@wei:~/share/Console$ php console generate:v
Please enter the view name :demo/category/index
> File is generated success!	../Cms/Application/Demo/View/Category/index.html
wei@wei:~/share/Console$
```

### 如何自定义模板

直接将template下对应的模板文件改成你想要的就行