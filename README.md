# easyexcel-demo

本demo主要是easyexcel的简单使用，并在基础上进行封装

项目是基于easyexcel的模板填充方式进行的，用户首先需要下载对应的模板，在模板中填充数据，
然后在进行导入操作；导出操作即easyexcel中的读excel。

项目结构
 - controller
 - service
 - listener
 - enums
 - util
 - entity

其中controller主要提供/download/{type}、/download/file/{type}、/upload/file/{type}三个接口

/download/{type}：下载模板
/download/file/{type}：下载文件 (导出)
/upload/file/{type}：上传文件（导入）

util包下的ExcelUtil是对EasyExcel类的简单封装，提供一系列外部参数，组合成对应的对象；

listener包下主要提供对不同Excel实体的读操作，切记该类不能使用spring管理

***
本项目中关键点在于建立对应的枚举，利用反射完成操作