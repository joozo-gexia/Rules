# H5Site Rule
Here are some of the rules for writing H5Site (responsive website).

#####//Written in 2015-05-29

写HTML时采用 less语法编写。最外层类名私有化命名。私有化命名（例如：jo-menu），私有化命名不超过两层嵌套，超过两层命名采用标准命名，如标题： .title ; 缩略图： thumbnail ; 这样的命名方式，增加模版可读性。

另外，less嵌套不超过4层。
###YES Code

	.jo-menu {
		margin:0 auto;
		.jo-nav {
			width:100%;
			
			.title {
				font-size:12px;
				&.a {color:#ccc;}
			}
			.subtitle {color:yellow;}
		}
	}

##Rules

1.模版引用 [csstoolkits.css In GitHub](http://github.com/bairongsoft/csstoolkits)，normalize.css,font-awesome.css

2.模版中类名命名的时候全局唯加前缀 jo- 

3.写HTML时板块区分明确，以保证写stl标签效率。

4.样式使用LESS编写，编辑器推荐HBUILDER ,时时自动编译less文件

5.尽量使用CSStoolkits里面的现成样式，以保证样式利用率。
