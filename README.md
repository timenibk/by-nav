# README

由于经常需要在不同的电脑不同的浏览器上操作，书签同步就很麻烦，所以想着写个导航页吧。

网站采用html+css+js+json 纯静态搭建，因为这么轻量的单页不想用框架不想用数据库。。可以直接扔阿里云的静态页托管

页面基础样式copy自<a target="_blank" href="https://github.com/geekape/geek-navigation">geekape</a>

页面截图：

![avatar](https://imgchr.com/i/JDnXng)

### 现已支持带自定义参数访问，参数格式如下：
http(s)://(url)/?p=(自定义json地址)&f=(自定义json分组)
页面示例：
![avatar](https://imgchr.com/i/JDurDg)

#### 自定义json结构（与原始json基本一致，删除desc简介，增加filter分组）：
```json
    [{
    "_id": "", //分类简称
	"classify": "", //分类名称
	"icon": "", //分类图标 基于themify-icons
	"sites": [{
		"name": "", //网站名
		"href": "",//网站链接
		"filter": "",//网站分类
		"logo": "" //网站logo
        }]
    }]
```
#### 自定义json结构说明
主要目标是为了工作与日常分离，在工作电脑上和自用电脑上使用不同json或分类；
可以使用不同json地址，或者同一json地址使用不同filter区分；
多个分类可以使用同一filter分组

#### 自定义参数地址跨域说明
如果使用别人搭建或本地调试页面，自定义url与导航页url不在同一个域名下，必须对自定义url开启允许跨域访问；
阿里云OSS开启跨域访问教程参考地址：
[https://help.aliyun.com/document_detail/31903.html?spm=a2c4g.11186623.2.15.3724c451vMxt3K#concept-pbw-4df-vdb]
其中来源 与header必填，不知道怎么填的直接*号，methods允许get与head；


TODO：
- [x] 网址带json地址参数访问（便于放一些不方便展示或杂乱的网页）；
- [ ] json网页可视化编辑页面（便于需要增加页面但不想手动编辑）；

# 其他说明 

- json中分类标题icon来自字体图标库[themify-icons](https://themify.me/themify-icons)；
- logo是我一分钟随手画的，应该没有侵权问题  吧；
- vscode文件夹是用vscode调试自动生成的，可以无视；
- 本项目基于MIT许可协议开源。