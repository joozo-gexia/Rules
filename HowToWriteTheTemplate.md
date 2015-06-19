# HTML 页面示例
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no" />
    <title> [标题随意] </title>
    <link href="css/docs.css" rel="stylesheet">
  </head>
  <body>
    <!--描述：第一部分--> 
    <div class="mo-menu">
      <div class="mo-max-width mo-menu-list">
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
> 模板新创建的类名都以 .mo-

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
