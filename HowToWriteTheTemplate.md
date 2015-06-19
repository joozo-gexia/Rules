# HTML 页面示例

> 页面横向分块，越细致越好

> 每个区块样式描述参考上面方式命名即可 

> 其它几个标准文件引用直接引用外部地址即可

> 类的命名要私有化，如：`.container` 需要在类前面加一个前缀 `mo-`,即 `.mo-container` ,私有化命名不超过两层嵌套，超过两层命名采用标准命名，如标题：`.title`; 缩略图： `.thumbnail`; 以增加模版可读性。

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no" />
    <title> 模版-｛%name%｝</title>
    <link href="http://cdn.bootcss.com/font-awesome/4.3.0/css/font-awesome.min.css" rel="stylesheet">
    <link href="http://cdn.bootcss.com/normalize/3.0.3/normalize.min.css" rel="stylesheet">
    <link href="http://ct.gexia.com/css/ct.min.css" rel="stylesheet">
    <!--上面3个文件直接使用外连接即可-->
    <link href="css/docs.css" rel="stylesheet">
  </head>
  <body>
    <!--描述：第一部分--> 
    <div class="mo-menu">
      <div class="mo-container mo-menu-list">
        <a href="#" class="active">首页</a>
        ....
        <a href="#">专属定制</a>
      </div>
    </div>

    <!--描述：第二部分-->
    <div class="mo-slogan">
      <img src="images/logo.png" alt="logo"/>
    </div>
        
    <!--描述：第 N 部分-->
    <div class="mo-copyright">
      版权所有 Copyright © 2003-2015 
    </div>
  </body>
</html>
```

# docs.less[docs.css] 样式表示例
> less嵌套不要超过三层

> 模板新创建的类名都以 `.mo-`

> 通用样式尽量少写，正常情况 `.mo-a` 不出现在通用样式里, 下面只是示例，原则是，当某个类会在多个分块里面出现，且样式呈现一致，我们这个时候会把这个类，放到通用样式里

* * *

```css
@charset 'UTF-8';

/*通用样式*/
.mo-container {
    max-width: 1200px; //设置页面最大宽度为1200px
    margin: 0 auto;    //设置元素水平居中
    padding:0 10px;    //设置内填充
    font-family: "Microsoft Yahei"; //设置字体为微软雅黑字体
}
/*其它通用样式*/
.mo-a {color:grey;}

/*-----------------------------------------------------*/
/*第一部分开始*/
.mo-menu {
  margin: 0;
  padding: 0;
  list-style: none;
  
  .mo-menu-list {
    padding: 30px 0;
    text-align: center;

    .mo-a {/*给所有a元素添加这个类*/
        display: inline-block;
        padding: 10px 50px;

        &:active,&.active {
          background: #2a9bd5;
        }
    }
  }   
}

/*第一部分 Pad样式*/
@media (min-width:768px) and (max-width:1000px) {
  .mo-menu {  
    .mo-a {
        padding: 10px 20px;
    } 
  }
}

/*第一部分 Phone样式*/
@media only screen and (max-width: 767px){
  .mo-menu {  
    .mo-a {
        padding: 10px 20px;
    }
  }
}
/*第一部分 结束*/

/*第二部分 开始*/
.mo-copyright {
    padding: 100px 0;
    text-align: center;
    background: #fff;
}
/*第一部分 Pad样式*/
@media (min-width:768px) and (max-width:1000px) {
  .mo-menu {  
    .mo-a {
        padding: 10px 20px;
    } 
  }
}
/*第二部分 Phone样式*/
@media only screen and (max-width: 767px){
  .mo-copyright {
    padding: 50px 0;
  }  
}
/*第二部分 结束*/
```

# CSS标准命名示例
```html
<div class="mo-container">
  头：header　　 
  内容：content/container　　 
  尾：footer　　 
  导航：nav　　 
  侧栏：sidebar 
  栏目：column　　 
  布局宽度：wrapper　　 
  左右中：left right center　　 
  登录条：loginbar　
  
  标志：logo　　 
  抽奖：raffle
  广告：banner　　 
  页面主体：main　　 
  热点：hot　　 
  新闻：news 
  下载：download　　 
  子导航：subnav　　 
  菜单：menu　　 
  子菜单：submenu　　 
  搜索：search　　 
  友情链接：friendlink　　 
  页脚：footer　　 
  版权：copyright　　 
  滚动：scroll　　 
  内容：content 
  标签页：tab 
  文章列表：list 
  提示信息：msg 
  小技巧：tips 
  栏目标题：title 
  加入：joinus 
  指南：guild 
  服务：service 
  注册：regsiter 
  状态态：status 
  投票：vote 
  合作伙伴：partner 
  
  导航：nav 
  主导航：mainbav 
  子导航：subnav 
  顶导航：topnav 
  边导航：sidebar 
  左导航：leftsidebar 
  右导航：rightsidebar 
  菜单：menu 
  子菜单：submenu 
  标题: title 
  摘要: summary
  标志：logo 
  广告：banner 
  登陆：login 
  登录条：loginbar 
  
  注册：regsiter 
  搜索：search 
  功能区：shop 
  标题：title 
  加入：joinus 
  状态：status 
  按钮：btn 
  滚动：scroll 
  标签页：tab 
  文章列表：list 
  提示信息：msg 
  当前的: current 
  小技巧：tips 
  图标: icon 
  注释：note 
  指南：guild 
  服务：service 
  热点：hot 
  新闻：news 
  下载：download 
  投票：vote 
  合作伙伴：partner 
  友情链接：link 
  版权：copyright
</div>
```
