---
title: 关于ie8的兼容性
tags: [前端]
categories: IT
description: sss
---
## 描述
在开发中，需要兼容ie8的情况，记录一下遇到的问题和解决方案
<!-- more -->

## bootstrap：
    只能使用2.0及以下版本

## jquery：
    只能使用1.x 版本

## js语句：
    严格要求书写，语法规范，属性结束时的逗号

## ie8 JSON未定义的问题：
    JSON是包含在JScript 5.8中，而为了向下兼容ie8只有在文档模式是”Internet Explorer 8 Standards”的时候才使用JScripte 5.8,其他时候使用JScripte 5.7特性。因此如果文档模式没有声明为”Internet Explorer 8 Standards”，ie8是找不到JSON对象的。因为没有兼容到ie6/7，所以必然在ie6/7中，JSON会出现未定义的问题。我项目中采用的是方法1，完美解决。

### 解决方法：
    引入定义json的文件json2.js， 
    下载地址：https://github.com/douglascrockford/JSON-js
    引入包含json的jQuery文件。
    如果不用兼容到ie6/7，只需要声明”Internet Explorer 8 Standards”模式，方法如下： 
    - 在文档头中添加<meta http-equiv="X-UA-Compatible" content="IE=8" >
    - 使用<!DOCTYPE>来声明文档

## console.log：
    ie8 执行会报错，程序不执行，打开F12，程序可执行，代码中删掉此语句

## ie8页面的编码问题：
    当IE右键不勾选自动选择编码的时候，IE是从解析页面标签优先再http header信息，而其他浏览器刚好相反。
    由于这个原因，title里如果包含了中文字符，就会导致编码自动选择成gb2312导致页面乱码或者空白。
    因此一定要把<meta http-equiv=Content-Type content="text/html; charset=utf-8">代码放在title标签之前。

## 静态文件编码和浏览器编码不一致：
    浏览器默认编码，将页面文件的字符集，修改一致