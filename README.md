# ES最佳实践
凝聚ERP高级开发实践经验和持续成果的免费项目——ESAP，来自村长的倾情奉献!

<p align="center">
  <img src="./img/logo.png" width="120">
</p>

## 什么是ESAP
* ESAP的全称是Eden Solution and Products，旨在打造殿堂级的信息化产品和解决方案。

* ESAP起源于2012年，最初由勤哲Excel服务器（ES）实现的，后来又借鉴汲取了著名的ERP系统——SAP R3的架构思想进行了重构。因此拥有了ES的灵活与SAP的强大。

* ESAP在过去的4年积攒沉淀了许多优秀的思想和技术，甚至超越了ES官方的更新速度，例如：2012年，ESAP就实现了模板级导航并用于生产，ES2013版才推出导航功能，并一直bug不断；2015年，ESAP配合golang实现了与微信对接，ES2016版才推出一个半成品的微信端。

## 下载地址

#### 最新版

* <a href="./build/esap2.5beta20.rar" target="_blank">esap2.5beta20.rar</a>

#### 稳定版

* x86版: <a href="./build/esap_x86.rar" target="_blank">esap2.4x86.rar</a>

* x64版: <a href="./build/esap_x64.rar" target="_blank">esap2.4x64.rar</a>

#### 文档&源码

* 官方文档 : [《ES最佳实践》](SUMMARY.md) 

* 文档Github仓库：[https://github.com/esap/esap.erp8.net](https://github.com/esap/esap.erp8.net) 欢迎提需求(玩家需求实现进度见[参考资料](ref.md))

#### ES模板

* 微信提醒(支持ES9.4+): <a href="./db/wechat_tmp.rar" target="_blank">wechat_tmp.rar</a> **微信模块配置步骤在[第七章](c7.md)**

* 邮件提醒(支持ES9.2+): <a href="./db/email_tmp.rar" target="_blank">email_tmp.rar</a> **相关示例在[第八章](c8.md)**

#### 示例数据库

* ES数据库: <a href="./db/esap2.0.rar" target="_blank">esap2.rar</a> Ver2.4

## 捐赠
维护这个项目需要大量时间和精力，如果它确实帮上了你的忙，不要忘了请我喝杯茶哦 :)

<p align="center">
  <img src="./img/esap_pay.png" width="400">
</p>

## ESAP项目构成
ESAP早已不再只是一套ERP级的ES模板，而是一套完整的生态，现在ESAP主要包括以下模块：

#### ES库备份
从ESAP提取的数据库核心框架，非常简单确又十分强大。

#### ES-API
对接ES库的API，不同于ESWEB，ES-API除了提供ES数据访问、工作流办理，还提供图片、附件访问，甚至包括官方没有的缩略图等接口功能。
>接口地址示例：`http://阿里云IP:9090/api`

#### 微信API
对接微信企业号的API，提供企业号应用接口功能，实现用户与ES对话式的交互。
>接口地址示例：`http://阿里云IP:9090/wx`

#### ES-APP
提供了移动端的访问，不同于官方2015版的简单APP，ES-APP采用了当下流行的Vue，nodejs等开源技术，提供了迅速定制实现任何复杂UI的可能。
>接口地址示例：`http://阿里云IP:9090/app`

#### ES-WebServer
提供专门为ES设计的Webserver，不依赖IIS，部署简单，所有配置一个db.json文件就搞定。

#### ES-desktop
提供桌面端B/S架构，通过定制可以实现任何需求，例如打开门禁或者是连接PLC显示生产线实时数据。

> 尽管看起来模块非常多，实际部署时仅仅只需要还原模板，再运行esap.exe就可以了，就是这么简单！

## ESAP的哲学
简单就是美，这个借口可以用一万年

## ESAP的未来
持续集成的社区力量，思想有多远，我们就能走多远！

## 开发环境
+ ES 9.4.124
+ SQL SERVER 2008R2

<hr />

## 更新日志

#### v2.5 里程碑！
公测中

* 微信提醒新增图片、文件消息支持；
* 微信提醒新增多人多部门消息支持；
* 微信提醒新增密图文消息支持，支持多条密图文；
* 微信提醒新增普通新闻消息支持，支持多条普通新闻；
* 新增微信签到，支持地图显示，支持菜单按钮签到；
* 新增微信图库，通过相册或拍摄照片上传，支持多图上传；
* 新增微信反馈，通过APP进行反馈提交；
* 微信超级查询新增回写支持，支持update,insert；
* 微信超级查询新增通讯录变量支持，增加任意标点分割功能；
* 微信超级查询新增多选混合权限支持；
* 微信超级查询新增任意应用回调支持；
* 微信超级查询新增扫码(二维码/条码)查询支持；
* 微信超级查询新增图片，附件查询支持；
* 微信超级查询新增OCR接口；
* 修复超级查询随机排序问题；
* 采用echo框架重构公共库。

#### v2.4 plus！
发布于`2017-2-4`

* 新增微信超级查询引擎；
* 新增API主机(Host),ESweb主机配置项；
* 新增工作流办理，plus!；
* 采用重构版微信SDK，plus!。

#### v2.3
发布于`2017-1-18`

* 新增微信提醒标题配置项；  
* 新增邮件提醒功能，可带图片、附件；  
* 修复高版本网盘系统表切换问题。

#### v2.2
发布于`2017-1-13`

* 简化配置项，增加配置页面/conf；  
* 更新大量细节，模块运行更稳定；
* 错误提示完善，不再因普通错误导致崩溃；  
* 现在你只需要两步就可以玩转微信提醒： **1、导入模板；2、启动esap.exe** 就是这么简单！

#### v2.1
发布于`2017-1-7`

* 修复BOM复制本表代码；  
* 更新vBOM、vPBOM视图，修复子件超过10个的RN排序问题；  
* 导入微信提醒、微信通讯录、微信提醒视图(vwxtx)；    
* 增加微信企业号API及基本配置； 

#### v2.0 
发布于`2017-1-5`

* 导入主数据：商品、企业、字典；  
* 导入IO单对象、订单对象；  
* 导入无级BOM；  
* 导入自动检查更新功能(ESAP_关于)。
