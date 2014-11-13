查看演示website立刻下载错误提交 填加用法

要求
jQuery版本在 1.9.0以上

兼容性
现代浏览器和移动平台上都能很好地支持，包括IE8和IE9表现得也很好。

用法

1、引入css和js文件
1
2
3
<script src="http://libs.baidu.com/jquery/1.9.1/jquery.min.js"></script>
<script type="text/javascript" src="jquery.onepage-scroll.js"></script>
<link href='onepage-scroll.css' rel='stylesheet' type='text/css'>

2、加入如下格式的 html标签
1
2
3
4
5
6
7
8
9
<body>
  ...
  <div class="main">
    <section>...</section>
    <section>...</section>
    ...
  </div>
  ...
</body>
注意上面的 section 标签，通过下面的js参数指定，即是我们的每一个页面的容器，

3、加入js代码
1
2
3
4
5
6
7
8
9
10
11
12
13
$(".main").onepage_scroll({
   sectionContainer: "section",     // 指定单页面的每个页面外部容器
   easing: "ease",                  // 页面切换的缓动效果，可设置成 "ease", "linear", "ease-in","ease-out", "ease-in-out"
   animationTime: 1000,             // 每个页面切换的时长
   pagination: true,                // 是否显示右边的导航圆形按钮
   updateURL: false,                // 切换页面的时候是否需要更新页面URL.
   beforeMove: function(index) {},  // 页面切换之前的回调，index表示页面的索引
   afterMove: function(index) {},   // 页面切换之后的回调，index表示页面的索引
   loop: false,                     // 当前页面为最后一个的时候，继续向下切换是否回到第一个页面
   keyboard: true,                  // 是否可以使用方向键来操纵页面切换
   responsiveFallback: false,        // 是否当浏览器宽度为某一个指定值的时候，去除该插件效果，如果想实现这种效果，那么可以指定一个宽度值
   direction: "vertical"            // 页面切换方向，可选值为 "vertical"水平 和"horizontal"垂直. 默认 "vertical"
 });
