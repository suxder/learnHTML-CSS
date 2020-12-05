# learnHTML-CSS
## 一、Typora

### 1.优雅的使用Typora

<<<<<<< HEAD
- 硬换行：你可以通过 `空格 + 空格 + Shift + Enter` 完成一次硬换行，而这也是许多 Markdown 编辑器所原生支持的。硬换行在文档被导出时将被保留，且没有换段的段后距。      
- Emoji:  在 Typora 中，你可以用 `:emoji:` 的形式来打出 emoji，软件会自动给出图形的提示，还是比较好用的。  
- Typora 原生支持 LaTeX 语法，你有两种方式输入 LaTeX 风格的数学公式：   
- 行内公式（inline）：用 `$...$` 括起公式，公式会出现在行内。    
- 块间公式（display）：用 `$$...$$` 括起公式（注意 `$$` 后需要换行），公式会默认显示在行中间。      
- 脚注在少数派的文章中也很常见，即某段话结尾右上角标有数字标记，页面底部进行注释的写法。你可以在需要插入脚注标号的位置写 `[^ number ]` ，再在下方通过 `[^ number ]:` 在文档中插入脚注。注意不要遗漏了脚注编号 `number` 前后的空格。  

=======

1. **硬换行:**你可以通过 `空格 + 空格 + Shift + Enter` 完成一次硬换行，而这也是许多 Markdown 编辑器所原生支持的。硬换行在文档被导出时将被保留，且没有换段的段后距。      

2. **Emoji:**在 Typora 中，你可以用 `:emoji:` 的形式来打出 emoji，软件会自动给出图形的提示，还是比较好用的。  

3. **Typora** 原生支持 LaTeX 语法，你有两种方式输入 LaTeX 风格的数学公式：   

4. **行内公式（inline）:**用 `$...$` 括起公式，公式会出现在行内。    

5. **块间公式（display）:**用 `$$...$$` 括起公式（注意 `$$` 后需要换行），公式会默认显示在行中间。      

6. **脚注**在少数派的文章中也很常见，即某段话结尾右上角标有数字标记，页面底部进行注释的写法。你可以在需要插入脚注标号的位置写 `[^ number ]` ，再在下方通过 `[^ number ]:` 在文档中插入脚注。注意不要遗漏了脚注编号 `number` 前后的空格。  

## 二、CSS

### 1.CSS 基本初始化：

```css
* {
    margin: 0;
    padding: 0;

}
```

*是代表所有html中的标签，{...}表示清除内外边距。  

```
ul {
    list-style: none;

}
```

HTML <ul> 标签：无序 HTML 列表

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

### 2.清除浮动及一些小细节

#### 1.清除浮动的原因以及方法：

[https://blog.csdn.net/zengyonglan/article/details/53304487]: 

#### 2.box-sizing: boder-box; 的使用原理：

在原有的盒模型中 **content =** **width**,**padding-right**,**padding-left**,**border-right**以及**border-left**属性之和  
使用box-sizing: boder-box 之后，width = content  
 **背景：**先声明一下运用的场景，假如项目布局使用的是**自适应**的布局方式，div给出的宽度是**百分比**的形式，即框占窗口宽度的50%，但边界和内边距是用像素来表示的怎么办？为了避免这种问题，可以使用属性**box-sizing**来调整框模型。使用**border-box**，来将框模型更改成这个新的模型。  

#### 3.display:  

CSS中display:block意思如下：  

- 如果bai用<div>+<a> 做一个du按钮，这个能理解吧，就zhi是 想通过dao link 来实现跳转，内但是看起来是容个按钮，且不需要触发事件。而且 css 也比 button 的好用。
- 这中情况下，如果不是“块”block，那么只要点到文字上时才会触发，点到 按钮<div>但是没点到字是不行的，但是用了 block 后，整个按钮都可以承载 a 的link操作了
- css中的display是设置元素显示的方式,block是一块状元素的方式显示，
- inline是以内联元素的方式显示，none是不不显示；
- 块状元素会单独占据一样，其他元素跟他在同一行的会被迫换行，挤到下一行那里去，inline则不会这样。

### 3.CSS选择符

#### 1.类型(元素)选择符

用于选择特定类型的元素，譬如段落：

```css
p {
	color: black
}
```

#### 2.后代选择符

后代选择符用于选择某个或者某组元素的后代

```css
blockquote p {
	padding-left: 2em
}
```

> 类型选择符与后代选择符非常适合全面应用基础样式。

Tip:后代选择符会选择一个元素的所有后代，包括该元素的儿子和孙子等。

```css
  <style>
    article p {
      font-weight: bold;
    }
  </style>
  <article>
    <h1>Hello,monica!</p>
      <h3>Hello,monica!</h2>
        <p>Hello,Tom!</p>
        <p>Hello,monica!</p>
        <p>Hello,Teddy</p>
  </article>
```

#### 3.ID选择符

```css
	#test {
		color: black
	}
	...
  <p id="test">
    I love u.
  </p>
```

> Tip: ID只能应用到页面中的一个元素，相当于人的身份证，一个人只能有一个身份证，一个人只能有身份证，每个人的身份证都不一样。

#### 4.类选择符

```css
  <style>
    .weight {
      font-weight: 900;
    }
    .size {
      font-size: 2em;
    }
  </style>
  ...
  <p class="weight size">
    Hello,monica!
  </p>
```

> Tip:类(class)就像人的名字或代号，一个人可以有多个名字或者代号。即一个元素标签可以绑定多个类。



## 三、HTML

### 一、web标准构成

> w3c和其它标准化组织指定的一系列标准的集合。

#### 1.结构标准：

对网页元素进行整理分类，主要包括**XML**和**XHTML**(e**X**tensible **H**yper**T**ext **M**arkup **L**anguage)。

#### **2.样式标准：**

设置网页元素的版式，颜色，大小等外观样式，主要指**CSS**。

#### 3.行为标准

网页模型的定义及交互的编写，主要包括DOM和ECMASCRIPT 两个部分。

### 二、HTML中的单标签

**<iamge\>、** **\<input\>、** **\<a\>** 、**\<base\>、**

<base> 标签为页面上的所有链接规定默认地址或默认目标。

通常情况下，浏览器会从当前文档的 URL 中提取相应的元素来填写相对 URL 中的空白。

使用 <base> 标签可以改变这一点。浏览器随后将不再使用当前文档的 URL，而使用指定的基本 URL 来解析所有的相对 URL。这其中包括 <a>、<img>、<link>、<form> 标签中的 URL。

**注释：**<base> 标签必须位于 head 元素内部。

### 三、HTML中的绝对路径与相对路径

#### 1.相对路径

./ ：代表文件所在的目录（通常情况下可以省略不写）

../ ：代表文件所在的父级目录（也就是上一级目录）

../../ ：代表文件所在的父级目录的父级目录（也就是上一级上一级目录）

/ ：代表文件所在的根目录

#### 2.绝对路径

如：<img src='https://www.taobao.com/img'/>表示绝对路径

### 四、列表标签

#### 1.无序列表

```html
	<ul>
        <li>百事可乐</li>
        <li>可口可乐</li>
        <li>炸鸡</li>
        <li>汉堡</li>
	</ul>
```

[![DBsECD.png](https://s3.ax1x.com/2020/11/26/DBsECD.png)](https://imgchr.com/i/DBsECD)

#### 2.有序列表

```html
     <ol>
        <li>百事可乐</li>
        <li>可口可乐</li>
        <li>炸鸡</li>
        <li>汉堡</li>
     </ol>
```

[![DBydQH.png](https://s3.ax1x.com/2020/11/26/DBydQH.png)](https://imgchr.com/i/DBydQH)

#### 3.自定义列表

```html
  <dl>
    <dt>芬达</dt>
    <dd>百事可乐</dd>
    <dd>可口可乐</dd>
    <dd>康师傅绿茶</dd>
    <dd>红茶</dd>
    <dd>橘子</dd>
    <dd>香蕉</dd>
  </dl>
```

[![DBcV8U.png](https://s3.ax1x.com/2020/11/26/DBcV8U.png)](https://imgchr.com/i/DBcV8U)

通过列表嵌套可以实现如图所示的结构：

[![DBcUrd.png](https://s3.ax1x.com/2020/11/26/DBcUrd.png)](https://imgchr.com/i/DBcUrd)

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<h2>千峰大食堂</h2>
		<ul>
			<li>卤肉菜
				<ul>
					<li>卤鸡肉</li>
					<li>卤鸭肉</li>
					<li>卤牛肉</li>
				</ul>
			</li>
			<li>
				盖浇饭
				<ul>
					<li>西红柿鸡蛋</li>
					<li>小炒肉</li>
					<li>鱼香肉丝</li>
				</ul>
			</li>
			<li>炒菜
				<ul>
					<li>蒜薹炒肉</li>
					<li>宫保鸡丁</li>
					<li>烧茄子</li>
				</ul>
			</li>
			<li>饮品
				<ul>
					<li>蜂蜜柚子茶</li>
					<li>冰糖雪梨</li>
					<li>可口可乐</li>
				</ul>
			</li>
		</ul>
	</body>
</html>
```

