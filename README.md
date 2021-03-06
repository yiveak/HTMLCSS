# HTML CSS

## HTML

| block elements ==== `display: block;`                        | inline elements ==== `display: inline;`                 | inline-block elements ==== `display: inline-block;` |
| ------------------------------------------------------------ | ------------------------------------------------------- | --------------------------------------------------- |
| `<div>` ====CSS布局常用                                      | `<span>` ====CSS布局常用                                | `<a>`                                               |
| `<form>` ---- 表单                                           | `<strong>` , `<em>` , `<del>` , `<ins>` ---- 文本格式化 |                                                     |
| `<table>` ---- 表格                                          | `<img>`                                                 |                                                     |
| `<ul>` , `<ol>` , `<li>` , `<dl>` , `<dt>` , `<dd>` ---- lists | `<label>` , `<input>`                                   |                                                     |
| `<h1>` , `<h2>` , `<h3>` , `<h4>` , `<h5>` , `<h6>` , `<p>`  | `<button>`                                              |                                                     |
| `<header>` , `<footer>` , `<nav>`                            | `<br>`                                                  |                                                     |
| `<section>`                                                  | `<textarea>`                                            |                                                     |

块级元素跟行内元素的区别：

* 块级元素独占一行，行内元素可一行可以多个。
* 块级元素可以设置宽、高、行高、外边距、内边距。行内元素可以设置行高，左右外边距跟左右内边距，不能设置宽、高、上下外边距跟上下内边距，其盒子的大小根据实际元素的内容确定(其宽度随着实际内容的变化而变化)。如果设置了行内元素的上下外边距、内边距，那么也不产生任何效果。

行内元素一般都是基于语义级(semantic)的基本元素，只能容纳文本或其他内联元素，常见内联元素 “a”

根据上下文环境可变的元素。





## HTML5

新增的语义化标签：`<header>`、 `<nav>`、  `<article>`、  `<section>`、  `<aside>`、  `<footer>`、

`<section>` 相当于是大号的 `<div>` 。

<img src=".\medias\SemanticHTML5.png" style="zoom:50%; "/>

多媒体标签：`<audio>` 、`<video>`

> 1. **`<video>`**
>
>    > ```html
>    > <!-- controls 控制播放的控件 -->
>    > <!-- 支持的格式mp4 webm ogg -->
>    > <video src = "" controls = "controls"></video>
>    > ```
>    >
>    > | 属性     | 值         | 描述                                                         |
>    > | -------- | ---------- | ------------------------------------------------------------ |
>    > | autoplay | autoplay   | 自动播放(谷歌浏览器得通过添加muted来解决自动播放的问题)      |
>    > | controls | controls   | 向用户显示播放控件  由于根据浏览器的不同，控件的样式也可能不同，所以实际开发中一般不直接设置，而通过JS设置成相同的控件样式 |
>    > | width    | npx        | 设置播放器的宽度                                             |
>    > | height   | npx        | 设置播放器的高度                                             |
>    > | loop     | loop       | 循环播放                                                     |
>    > | preload  | auto, none | 是否预先加载视频，如果有了autoplay，则忽略该属性             |
>    > | src      | url        | 视频url地址                                                  |
>    > | poster   | imgurl     | 加载等待的画面图片                                           |
>    > | muted    | muted      | 静音播放                                                     |
>
> 2. **`<audio>`**
>
>    > ```html
>    > <audio src = ""></audio>
>    > ```
>    >
>    > | 属性     | 值       | 描述                                    |
>    > | -------- | -------- | --------------------------------------- |
>    > | autoplay | autoplay | 设置自动播放 谷歌浏览器默认禁用自动播放 |
>    > | controls | controls | 控制播放音频的控件                      |
>    > | loop     | loop     | 循环播放                                |
>    > | src      | url      | 音频文件的地址                          |



新增的 `<input>` 类型(type)

| 属性值              | 说明                                 |
| ------------------- | ------------------------------------ |
| type = "email"      | 限制用户必须输入email类型            |
| type = "url"        | 限制用户必须输入url类型              |
| type = "date"       | 限制用户必须输入日期类型，日期选项卡 |
| type = "time"       | 限制用户必须输入时间类型，时间选项卡 |
| type = "month"      | 限制用户必须输入月类型               |
| type = "week"       | 限制用户必须输入周类型               |
| **type = "number"** | 限制用户必须输入数值类型             |
| **type = "tel"**    | 手机号码                             |
| **type = "search"** | 搜索框                               |
| type = "color"      | 生成一个颜色选择表单                 |

验证的时候必须添加表单域，即：

```html
<form action = "">
    <ul>
        <li>邮箱：<input type = "email"></li>
        <li>URL：<input type = "url"></li>
        <li>日期：<input type = "date"></li>
        <li>手机号：<input type = "tel"></li>
        <li>数字：<input type = "number"></li>
        <li>搜索：<input type = "search"></li>
        <li>颜色：<input type = "color"></li>
        <!-- 当点击提交时，就能验证表单 -->
        <li><input type = "submit" value = "提交"></li>
    </ul>
</form>
```

新增的**表单属性**

| 属性            | 值        | 说明                                                         |
| --------------- | --------- | ------------------------------------------------------------ |
| required        | required  | 表示该表单必填                                               |
| **placeholder** | 提示文本  | 表单的提示信息，存在默认值将不显示                           |
| autofocus       | autofocus | 页面加载完后鼠标自动聚焦到该表单                             |
| autocomplete    | off, on   | 当用户开始输入时，浏览器基于历史输入，显示该表单中输入过的内容。需要放在表单内，且加上name属性，同时成功提交过 |
| **multiple**    | multiple  | 多选文件提交上传 通常跟文件域搭配使用                        |

```css
/* 通过伪元素修改样式 */
input::placeholder {
    color: orange;
}
```



## CSS

### 选择器

#### 选择器



#### 选择器的权重

> 1. **层叠性** ：就近原则
>
> 2. **继承性** ：继承父元素的样式
>
>    > 可从父元素继承的样式是**与文字相关的样式**，比如字体颜色、大小、字体，字体水平位置，字体的行高。
>    >
>    > 并不包括，父元素的行高(height)、宽(width)
>
> 3. **优先级**
>
>    > * 选择器相同，则按层叠性执行
>    >
>    > * 选择器不同，则根据选择的权重执行
>    >
>    >   |                      |                  |
>    >   | -------------------- | ---------------- |
>    >   | 元素选择器           | 0, 0, 0, 1       |
>    >   | 类选择器、伪类选择器 | 0, 0, 1, 0       |
>    >   | ID选择器             | 0, 1, 0, 0       |
>    >   | 行内样式             | 1, 0, 0, 0       |
>    >   | `!important`         | Infinity，无穷大 |
>    >
>    >   





页面布局，3大核心：盒子模型、浮动、定位。

> 1. 准备好相关的网页元素，比如`<div>` 、`<ul>` 、`<li>` 、`<a>` ......
> 2. 利用CSS设置盒子的样式，且将盒子放到相应的位置
> 3. 往盒子里放内容

* **盒子模型** ：封装周围的HTML元素，A Box。

  > 盒子模型的组成：**内外边距(margin, padding)**、**边框(border)**、**实际内容(content)**。
  >
  > * **外边距(margin)** ：盒子跟盒子之间的距离。
  > * **内边距(padding)** ：盒子里的实际内容到该盒子边框的距离。
  > * **边框(border)** ：盒子边框的粗细大小(px)、样式(solid, dashed, dotted...)、颜色。
  >   * `border-collapse` ：合并相邻两个盒子的边框(细线边框)。



### 浮动

浮动元素跟标准流的父元素搭配使用。

* 设置父盒子是有高度的

* 所有的父盒子都必须有高度吗？ ---- 很多情况下父盒子不方便给高度，因为不知道有多少子盒子。

  > 理想中的状态，让子盒子撑开父盒子，有多少子盒子，父盒子就有多高
  >
  > > 如果子盒子都设置高度，且都设置了浮动，则造成了父盒子的"**高度塌陷**"(父盒子的高度为0，且影响下面的标准流盒子布局)，这是因为浮动的盒子脱标且不占有原先文档流的位置。
  > >
  > > 所以，这时候就要：**清除浮动**

清除浮动：清除浮动元素造成的影响。

>  **清除浮动之后，父级就会根据浮动的子盒子自动检测其高度，即父级有了高度，那么也就不影响下面的标准流盒子布局。**
>
> > 语法：
> >
> > ```
> > 选择器{clear: 属性值;}
> > ```
> >
> > 属性值：
> >
> > | 属性值   | 描述                                     |
> > | -------- | ---------------------------------------- |
> > | left     | 不允许左侧有浮动元素(清除左侧浮动的影响) |
> > | right    | 不允许右侧有浮动元素(清除右侧浮动的影响) |
> > | **both** | 同时清除左右两侧浮动元素的影响           |
>
> 清除浮动的策略是：**闭合浮动**
>
> **清除浮动的方法** ：
>
> > 1. **额外标签法** ---- 隔墙法，W3C推荐
> >
> >    > 额外标签法：**在浮动元素末尾添加一个空的标签(必须是块级元素)**。
> >    >
> >    > ```css
> >    > .clear {
> >    > 	clear: both;
> >    > }
> >    > ```
> >    >
> >    > 缺点：添加许多无意义的标签，结构性差。
> >
> > 2. **给父级添加overflow属性**
> >
> >    > 属性值：`hidden` ，`auto` ，`scroll`
> >    >
> >    > ```css
> >    > .father_box {
> >    >     overflow: hidden;
> >    > }
> >    > ```
> >    >
> >    > 缺点：**无法显示溢出的部分** 。
> >
> > 3. **给父级添加after伪元素**
> >
> >    > ```css
> >    > .clearfix:after {
> >    >     content: "";
> >    >     display: block;
> >    >     height: 0;
> >    >     clear: both;
> >    >     visibility: hidden;
> >    > }
> >    > 
> >    > .clearfix { /* IE6, 7 */
> >    >     *zoom: 1;
> >    > }
> >    > ```
> >
> > 4. **给父级添加双伪元素**
> >
> >    > ```css
> >    > .clearfix:before, .clearfix:after{
> >    >     content: "";
> >    >     display: block;
> >    > }
> >    > .clearfix:after {
> >    >     clear: both;
> >    > }
> >    > .clearfix {
> >    >     *zoom: 1;
> >    > }
> >    > ```



CSS属性书写顺序(重点)：

> 1. **布局定位属性**
>
>    ```
>    display(第一个，关系到模式), position, float, clear, visibility, overflow
>    ```
>
> 2. **自身属性**
>
>    ```
>    width, height, margin, padding, border, background
>    ```
>
> 3. **文本属性**
>
>    ```
>    color, font, text-decoration, text-align, vertical-align, white-space, breakword
>    ```
>
> 4. **其他属性(CSS3)**
>
>    ```
>    content, cursor, border-radius, box-shadow, text-shadow, background: linear-gradient...
>    ```
>
> * 参考
>
>   ```css
>   .example {
>   	display: block;
>   	position: relative;
>   	float: left;
>   	width: 100px;
>   	height: 200px;
>   	margin: 0 10px;
>   	padding: 20px 0;
>       /* 
>       注意：其中不需要设置的属性可以省略（取默认值），但必须保留font-size和font-family属性，否则font属性将不起作用。		*/
>   	font: font-style font-weight font-size/line-height font-family;
>    	/* background:背景颜色 背景图片地址 背景平铺 背景滚动 背景位置 */   
>   	background: rgba(0, 0, 0, .3) url("") no-repeat scroll;
>   	border-radius: 5px;
>   }
>   ```



网页页面布局的整体思路：

> 1. 确认页面的版心。
> 2. 分析页面中的行模块，以及每个行模块中的列模块，即页面布局的第一准则。
> 3. 一行中列模块经常通过浮动布局，先确定每个列的大小，然后确定列的位置，即页面的第二准则。
> 4. 制作HTML结构，先结构后样式，结构永远最重要。
> 5. **一定先理清布局结构**，然后写代码。



实际开发中，导航栏是通过`li` + `a` 的做法 

```html
<div class="nav">
    <ul>
        <li><a href="#">首页</a></li>
    </ul>
</div>
```

如果导航栏一行显示，那么给 `li` 添加浮动，因为 `li` 是块级元素。

导航栏不给宽度，是因为后期可以添加其余的导航条目。

因为导航里的文字内容字数不同，所以最好给 `a` 左右padding撑开盒子，而不是指定宽度。

行内块元素同行显示时，之间默认有个空隙，通过 `float: left` 可以无空隙。



### 定位

> 定位：按照定位的方式移动/摆放盒子。
>
> **定位 = 定位模式 + 边偏移**
>
> > **定位模式** ： 指定一个元素在文档中的定位方式。
> >
> > > 通过 `position` 属性来设置，其值有：**static** 、**relative** 、**absolute** 、**fixed(固定的)** 、**`sticky`**
> > >
> > > * `selector { position: static; }` (了解)
> > >
> > >   > 按照标准流摆放位置，无边偏移。(布局很少用)
> > >
> > > * **`selector { position: relative; }` (重要)**
> > >
> > >   > 相对于该元素原来位置的定位(移动位置)，即 **移动的参照点是该元素原来的位置，且该元素原有的位置仍被其占有**。
> > >   >
> > >   > ```css
> > >   > .box {
> > >   >     /* 该盒子原有的位置仍被其占有，即不脱标 */
> > >   >     position: relative;
> > >   >     /* 注意要加边偏移，定位 = 定位模式 + 边偏移 */
> > >   >     top: 50px;
> > >   >     left: 50px;
> > >   > }
> > >   > ```
> > >   >
> > >   > **子绝父相** ：子盒子绝对定位，其父盒子必须相对定位。
> > >   >
> > >   > > * 子盒子绝对定位，不占有位置，可以在父盒子中的任何位置进行摆放，不影响其他兄弟盒子。
> > >   > > * 父盒子加定位，可以让子盒子限制在父盒子内
> > >   > > * 父盒子布局时，需要占据原有的位置，所以给父盒子设置的是相对定位，绝对定位不保留原先的位置。
> > >
> > > * **`selector { position: absolute; }` (重要)**
> > >
> > >   > 相对该元素的 **祖先元素** 来移动位置(进行定位)。
> > >   >
> > >   > **绝对定位的3个特点(重点)**：
> > >   >
> > >   > > * 如果 **没有祖先元素** ，或者 **祖先元素没有定位** ，则以 **浏览器** 为准进行定位(即 **Document文档** )。
> > >   > >
> > >   > > * 如果 **祖先元素有定位(相对、绝对、固定)** ，则以 **最近一级的有定位的祖先元素** 为参考点进行移动定位。
> > >   > >
> > >   > >   > 所以，怎么约束绝对定位的盒子在父盒子里头？子绝父相。
> > >   > >
> > >   > > * 绝对定位 **不再占有原有的位置**，**脱标**。
> > >
> > > * **`selector { position: fixed; }`  (重要)**
> > >
> > >   > **特点** ：
> > >   >
> > >   > * 以 **浏览器的可视窗口** 为参照点进行移动定位。
> > >   >
> > >   >   > * 跟父级元素没有任何关系
> > >   >   > * 不随滚动条的滚动而滚动，是固定在页面中的
> > >   >
> > >   > * 固定定位 **不占有原先的位置** ， 即 **脱标** 。(可以看作是一种特殊的绝对定位)
> > >
> > > * **`selector { position: sticky; }`  **
> > >
> > >   > 可以看作是相对定位和固定定位的混合
> > >   >
> > >   > **特点** ：
> > >   >
> > >   > * 以 **浏览器的可视窗口** 为参照点进行移动定位。(固定定位的特点)
> > >   > * 粘性定位 **占有原先的位置** 。(相对定位的特点)
> > >   > * 必须添加 `top` 、`bottom` 、 `left` 、`right` 四个属性中的至少一个才有效。如果不设置，则被视为相对定位。
> >
> > **边偏移** ：决定该元素的最终位置。
> >
> > > 通过 `top` 、`bottom` 、 `left` 、`right` 四个属性来设置
> > >
> > > | 边偏移属性 | 示例 (也可以设置百分比) |                                                      |
> > > | ---------- | ----------------------- | ---------------------------------------------------- |
> > > | `top`      | `top: 80px;`            | **顶端**偏移量，定义元素相对其父元素**上边线的距离** |
> > > | `bottom`   | `bottom: 90px;`         | **底部**偏移量，定义元素相对其父元素**下边线的距离** |
> > > | `left`     | `left: 50px;`           | **左侧**偏移量，定义元素相对其父元素**左边线的距离** |
> > > | `right`    | `right: 50px;`          | **右侧**偏移量，定义元素相对其父元素**右边线的距离** |
>
> **定位叠放次序 z-index**
>
> > 控制盒子叠放的前后(上下)次序(z轴)。
> >
> > **`selector { z-index: 1; }`** ，取值可以是：正整数、负数、0，默认是auto，数值越大，盒子越是上面。
> >
> > * 如果其属性值相同，则按照后来居上的原则
> > * 数值后面不能加单位
> > * 只有定位的盒子才有 `z-index` 属性
>
> **定位的特殊性**
>
> > * 行内元素如果添加了绝对或者固定定位，那么可以直接设置高度、宽度。
> > * 块级元素如果添加了绝对或者固定定位，如果不给宽度高度，那么默认是实际内容的大小。
> > * 浮动元素、绝对定位( or 固定定位 )元素，(脱离标准流)都不会造成外边距合并的问题( 外边距塌陷 )。
> > * 绝对定位(or 固定定位)会完全压住下面的盒子以及其里面的任何内容。但浮动元素则只会压住下面标准流的盒子，而不会压住下面标准流盒子内的文字内容(图片)。

如何让绝对定位的盒子水平居中？先向左(右)走父盒子宽度的50%，然后向左(右)走其本身盒子宽度的50%。

### 标准流、浮动、定位

> 1. **标准流** ：垂直的块级盒子显示，就使用标准流。
> 2. **浮动** ：多个块级盒子同行显示，就使用浮动。
> 3. **定位** ： 如果某元素(盒子)要在某个盒子内任意移动，就使用定位。定位最大的特点是有层叠的概念。



#### 元素的显示与隐藏

> **`display`** 、 **`visibility`** 、**`overflow`**
>
> 1. **`diplay`**
>
>    >`display` 属性：设置一个元素如何显示。(不保留该元素原先的位置)
>    >
>    >```
>    >display: none; /* 隐藏 隐藏后元素不占有原先的位置 并没有被删除*/
>    >display: block; /* 显示 块级显示*/
>    >display: inline-block;
>    >display: inline;
>    >...
>    >/* none, block搭配JS实现很多网页特效 */
>    >```
>
> 2. **`visibility`**
>
>    > **可见性** ：保留原先的位置
>    >
>    > ```
>    > visibility: inherit; /* 如果父级可见，则继承父级的可见性 */
>    > visibility: visible; 
>    > visibility: hidden; /* 对象隐藏，但是继续占有原先的位置 */
>    > visibility: collpase; /* 主要用来隐藏表格的行或列 */
>    > ```
>
> 3. **`overflow`**
>
>    > **溢出隐藏** ：即对溢出(超过其指定的宽高)的部分做了什么样的事情。
>    >
>    > ```
>    > overflow: visible;
>    > overflow: hidden;
>    > overflow: scroll; /* 总是显示滚动条 即使不内容溢出*/
>    > overflow: auto; /* body, textarea的默认值 在必须(需要)的时候显示滚动条*/
>    > ```
>    >
>    > **如果有定位的盒子，慎用 `overflow: hidden;` ，因为它会隐藏多余的部分。** 
>    >
>    > > 例如：如果这里使用 `overflow: hidden` ，那么hot这个小图标则显示不出来。
>    > >
>    > >  <img src="./medias/OverflowHiddenCareful.png" alt="NO Overflow:hidden;" style="zoom:65%;" />



#### 精灵图sprites

> 精灵技术主要针对于背景图片使用，多个小背景图整合成一张大图。
>
> 如何移动到背景图片的位置？`background-position: x轴值 y轴值;`
>
> > 移动的是这个目标图片的X轴、Y轴坐标，往上、左移动都是负值。(一般情况下，精灵图移动的距离都是负值)
> >
> > 精确测量每个小背景图的位置。



#### 字体图标iconfont

> iconfont：看起来像是个图标，但本质是个文字。
>
> 优点：适合结构样式简单的小图标，复杂结构样式的仍需要精灵图。
>
> * 轻量，一个字体图标比一个图像小，渲染快，减少服务器的请求
> * 灵活性，可以修改样式，比如颜色、大小
> * 兼容性



#### CSS三角

```css
/* 盒子的宽高必须设置为0 */
/* 三角形的大小取决于边框多少px */
.box {
    width: 0;
    height: 0;
    /* 下面2行代码兼容低版本浏览器 */
    line-height: 0;
    font-size: 0;
    border-top: 50px solid red;
    border-right: 50px solid green;
    border-bottom: 50px solid yellow;
    border-left: 50px solid blue;
    
}

/* 一个等腰三角形，让其他三角形透明 */
.box {
    width: 0;
    height: 0;
    line-height: 0;
    font-size: 0;
    border: 50px solid transparent;
    /* 改颜色 */
    border-bottom-color: orange;
}

/* 等腰直角三角形 */
.box {
    width: 0;
    height: 0;
    line-height: 0;
    font-size: 0;
    border: 50px solid transparent;
    border-right-color: orange;
    border-bottom-color: orange;
}
```



#### CSS用户界面样式

>  	1. **更改用户的鼠标样式**
>
> > `selector { cursor: pointer; }`
> >
> > | 属性值         | 描述               |
> > | -------------- | ------------------ |
> > | **default**    | 默认样式，小白箭头 |
> > | **pointer**    | hand               |
> > | **move**       | 移动               |
> > | **text**       | 文本               |
> > | **notallowed** | 禁止               |
>
> 2. **表单轮廓线 outline**
>
>    > `outline: none;` ，比如 `input`、`textarea`
>    >
>    > ``` css
>    > /* 取消表单轮廓 */
>    > input,
>    > textarea {
>    >     outline: none;
>    > }
>    > ```
>
> 3. **防止文本域拖拽 resize**
>
>    > ```css
>    > textarea {
>    >     resize: none;
>    > }
>    > ```
>
> 4. **`vertical-align`**
>
>    > 常用于设置，图片或者表单(行内元素)和文字垂直对齐。(只针对行内元素、行内块元素)。
>    >
>    > ```css
>    > vertical-align: baseline(基线) | top(顶线) | middle(中线，常用) | bottom(底线)
>    > 
>    > /* 常见搭配使用 */
>    > selector {
>    >     display: inline-block;
>    >     vertical-align: middle;
>    > }
>    > ```
>    >
>    > 且，可以解决图片底部的空白缝隙，因为**行内块/行内元素默认是以文字的基线对齐的**。
>    >
>    > * 方式1，通过给图片设置 `vertical-align` 属性，其取值四个皆可。(推荐)
>    > * 方式2， 给图片设置 `display: block;` ，因为块级元素不以文字的基线对齐。
>
> 5. **溢出的文字由省略号代替** ---- 后台更方便控制
>
>    > 1. **单行文本溢出，显示省略号**
>    >
>    >    > 必须先满足3个条件：
>    >    >
>    >    > ```css
>    >    > /* 1. 先强制一行内显示文本 默认normal，即自动换行*/
>    >    > white-space: nowrap;
>    >    > /* 2. 超出部分隐藏 */
>    >    > overflow: hidden;
>    >    > /* 3. 超出文字用省略号代替 */
>    >    > text-overflow: ellipsis;
>    >    > ```
>    >
>    > 2. **多行文本溢出，显示省略号**
>    >
>    >    > ```css
>    >    > overflow: hidden;
>    >    > text-overflow: ellipsis;
>    >    > /* 弹性伸缩盒子模型显示 */
>    >    > display: -webkit-box;
>    >    > /* 限制在一个块元素显示的文本的行数 省略号在哪行的意思*/
>    >    > -webkit-line-clamp: 2;
>    >    > /* 设置或检索伸缩盒对象的子元素的排列方式 */
>    >    > -webkit-box-orient: vertical;
>    >    > ```
>    >    >
>    >    > 兼容性问题，适合移动端，即WebKit内核



#### 常见布局技巧

>  1. **margin负值的运用**
>
>     > float AB两个盒子，A盒子的左边框跟B盒子的右边框重叠，其值变为2px(假设边框1px)，那么如何使得重叠的边框为1px？
>     >
>     > 即，让B盒子多向左magrin -1px的距离，则得到细线边框。
>
>  2. **文字围绕浮动元素**
>
>     > `float` 
>
>  3. **行内块的巧妙运用**
>
>     > 页码 (给该行内块的父盒子添加t`text-align: center;` ，那么其中的盒子自然而然的居中对齐了)
>     >
>     > 行内块本身就有大小，且之间有距离
>
>  4. **CSS三角强化**
>
>     > 直角三角形(一条直角边长，一条直角边短)
>     >
>     > ```css
>     > .box {
>     > 	width: 0;
>     > 	height: 0;
>     > 	line-height: 0;
>     > 	font-size: 0;
>     > 	border-color: transparent orange transparent transparent;
>     > 	border-style: solid;
>     > 	border-width: 24px 10px 0 0;
>     > }
>     > ```



## CSS3

新增的选择器、盒子模型、其他特性

**新增的选择器**

> 1. **属性选择器**  (选择器权重为10)
>
>    > 根据**元素特定的属性**来选择元素。`[]` 
>    >
>    > | 选择符              | 说明                                          |
>    > | ------------------- | --------------------------------------------- |
>    > | E [att]             | 选择具有att属性的E元素                        |
>    > | **E [att = "val"]** | 选择具有att属性且其属性值等于val的E元素       |
>    > | E [att ^="val"]     | 匹配具有att属性且其属性值以val**开头**的E元素 |
>    > | E [att $="val"]     | 匹配具有att属性且其属性值以val**结尾**的E元素 |
>    > | E [att *="val"]     | 匹配具有att属性且其属性值中含有val的E元素     |
>
> 2. **结构伪类选择器** (选择器权重为10)
>
>    > 根据**文档的结构**来选择，常用于根据父级选择器里面的子元素
>    >
>    > | 选择符                                                       | 说明                          |
>    > | ------------------------------------------------------------ | ----------------------------- |
>    > | E: first-child                                               | 匹配父元素中的第一个子元素E   |
>    > | E: last-child                                                | 匹配父元素中的最后一个子元素E |
>    > | **E: nth-child(n)**  n可以是数字，公式，关键词(even、odd...) | 匹配父元素中的第n个子元素E    |
>    > | E: first-of-type                                             | 指定类型E的第一个             |
>    > | E : last-of-type                                             | 指定类型E的最后一个           |
>    > | E: nth-of-type(n)                                            | 指定类型E的第n个              |
>    >
>    > ```css
>    > /* css隔行变色 E:nth-child(n) */
>    > ```
>    >
>    > | n的公式 --- n从0开始取值 | 取值                         |
>    > | ------------------------ | ---------------------------- |
>    > | 2n                       | 偶数                         |
>    > | 2n+1                     | 奇数                         |
>    > | 5n                       | 5，10，15...                 |
>    > | n+5                      | 从第5个开始到最后，包含第5个 |
>    > | -n+5                     | 前5个，包含第五个            |
>    >
>    > `E: nth-child(n)` 跟 `E: nth-of-type(n)` 的区别
>    >
>    > > 前者，将所有的子盒子都排列序号
>    > >
>    > > 后者，将指定元素的盒子排列序号
>    > >
>    > > ```html
>    > > <style>
>    > >     <!-- 一个元素都未改变字体颜色 -->
>    > >     <!-- nth-child(n)将所有的子盒子排号，即p是0，熊大div是1，熊二div是2-->
>    > >     section div:nth-child(1){ <!-- 总权重为12，结构伪类选择器的权重10，div的权重为1，section的权重为1-->
>    > >         color: orange;
>    > >     }
>    > >     <!-- 熊大改变字体颜色 -->
>    > >     section div:nth-of-type(n){
>    > >         color: yellow;
>    > >     }
>    > > </style>
>    > > 
>    > > <body>
>    > >     <section>
>    > >     	<p>光头强</p>
>    > >         <div>熊大</div>
>    > >         <div>熊二</div>
>    > >     </section>
>    > > </body>
>    > > ```
>
> 3. **伪元素选择器**  (选择器权重为1)
>
>    > 可以利用CSS创建新的标签元素，而不需要HTML标签，从而简化HTML的结构。`::`
>    >
>    > | 选择符   | 说明                     |
>    > | -------- | ------------------------ |
>    > | ::before | 在元素内部的前面插入内容 |
>    > | ::after  | 在元素内部的后面插入内容 |
>    >
>    > > * before，after会创建一个**行内元素**
>    > > * 新创建的这个行内元素**在文档树中是找不到的**，所以称之为 **伪元素**
>    > > * 语法：`element::before {}`
>    > > * before，after必须有**content属性**。
>    > > * 伪元素选择器的权重，跟标签选择器一样，为1。



**盒子模型**

> 通过 `box-sizing` 来指定盒子模型，有2个值：`content-box` ，`border-box` 。
>
> > `box-sizing: content-box; ` 这样盒子大小 = width + padding + border (就是以前默认的样式计算)。
> >
> > `box-sizing: border-box;` 这样**盒子大小 = width**。
> >
> > * 这也就意味着，设置padding跟border就不会撑开大盒子 ---- 前提是padding和border相加不超过width。



**模糊图片 filter**

> `filter` (滤镜) 将模糊、颜色偏移等图形效果应用于元素。
>
> ```css
> filter: 函数();
> 
> filter: blur(5px); /* 其中数值越大，越模糊。注意要加单位px */
> ```

**`width: calc`函数**

> 计算盒子的宽度。
>
> ```css
> width: calc(100% - 80px);
> 
> 
> /* 例如，让父盒子宽度永远比子盒子大30px */
> .parent {
>     width: 300px;
>     height: 100px;
> }
> 
> .child {
>     width: calc(100% - 30px);
>     height: 100%;
> }
> ```



**过渡属性** (重点)

> **`transition`** ，可以在不使用Flash动画或JavaScript的情况下，为元素从一种变成另一种样式时添加效果。
>
> 过渡动画，从一个状态渐渐过渡到另一个状态。**经常跟 `:hover` 搭配使用**。
>
> ```
> transition: 要过渡的属性 花费的时间 运动曲线 何时开始;
> 
> 1. 属性：想要变化的CSS属性，比如宽高、背景颜色、内外边距...如果是所有的属性都变化过渡，则写一个'all'。
> 2. 花费的时间：单位是秒，必须写单位's'。
> 3. 运动曲线：默认是'ease'，可省略。
> 4. 何时开始： 单位是秒，可以设置延迟触发时间，默认是0s(可省略)。
> 
> 多个属性
> transition: width .5s, height .5s; /* 逗号分隔 */
> transition: all .5s;
> ```

