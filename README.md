[TOC]

# 形状

## 矩形

<rect> 标签可用来创建矩形，以及矩形的变种

- rect 元素的 width 和 height 属性可定义矩形的高度和宽度
- x,y 属性定义矩形的左上角偏移量,
- rx 和 ry 属性可使矩形产生圆角。
- style 属性用来定义 CSS 属性
- CSS 的 fill 属性定义矩形的填充颜色（rgb 值、颜色名或者十六进制值）
- CSS 的 stroke-width 属性定义矩形边框的宽度
- CSS 的 stroke 属性定义矩形边框的颜色
- CSS 的 fill-opacity 属性定义填充颜色透明度（合法的范围是：0 - 1）
- CSS 的 stroke-opacity 属性定义笔触颜色的透明度（合法的范围是：0 - 1）

```html
<svg
  width="100%"
  height="100%"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
>
  <rect
    x="20"
    y="20"
    rx="20"
    ry="20"
    width="250"
    height="100"
    style="fill: red; stroke: black; stroke-width: 5; opacity: 0.5"
  />
</svg>
```

## 圆形

<circle> 标签可用来创建一个圆。

- cx 和 cy 属性定义圆点的 x 和 y 坐标。如果省略 cx 和 cy，圆的中心会被设置为 (0, 0)
- r 属性定义圆的半径。

```html
<svg
  width="100%"
  height="100%"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
>
  <circle
    r="40"
    cx="100"
    cy="50"
    stroke="orange"
    stroke-width="2"
    fill="indianred"
  />
</svg>
```

## 椭圆

<ellipse> 标签可用来创建椭圆。

- cx 属性定义圆点的 x 坐标
- cy 属性定义圆点的 y 坐标
- rx 属性定义水平半径
- ry 属性定义垂直半径

```html
<svg
  width="100%"
  height="100%"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
>
  <ellipse cx="240" cy="100" rx="220" ry="30" style="fill: purple" />
  <ellipse cx="220" cy="70" rx="190" ry="20" style="fill: lime" />
  <ellipse cx="210" cy="45" rx="170" ry="15" style="fill: yellow" />
</svg>
```

## 线条

<line> 标签用来创建线条。

- x1 属性在 x 轴定义线条的开始
- y1 属性在 y 轴定义线条的开始
- x2 属性在 x 轴定义线条的结束
- y2 属性在 y 轴定义线条的结束

```html
<svg
  width="100%"
  height="100%"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
>
  <line
    x1="0"
    y1="0"
    x2="300"
    y2="300"
    style="stroke: indianred; stroke-width: 2"
  ></line>
</svg>
```

## 多边形

<polygon> 标签用来创建含有不少于三个边的图形。

points 属性定义多边形每个角的 x 和 y 坐标

```html
<svg width="100%" height="600" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <polygon
    points="220,100 300,210 170,250 123,234"
    style="fill: #cccccc; stroke: #000000; stroke-width: 1"
  />
</svg>
```

## 折线

<polyline> 标签用来创建仅包含直线的形状。

points 属性定义折线每个连接点的 x 和 y 坐标

```html
<svg
  width="100%"
  height="100%"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
>
  <polyline
    points="0,0 0,20 20,20 20,40 40,40 40,60"
    style="fill: white; stroke: indigo; stroke-width: 4"
  />
</svg>
```

## 路径

<path> 标签用来定义路径。

下面的命令可用于路径数据：

- M = moveto
- L = lineto
- H = horizontal lineto
- V = vertical lineto
- C = curveto
- S = smooth curveto
- Q = quadratic Belzier curve
- T = smooth quadratic Belzier curveto
- A = elliptical Arc
- Z = closepath

注释：以上所有命令均允许小写字母。大写表示绝对定位，小写表示相对定位。

```html
<svg
  width="100%"
  height="100%"
  viewBox="0 0 400 400"
  xmlns="http://www.w3.org/2000/svg"
>
  <path
    d="M 100 100 L 300 100 L 200 300 z"
    fill="orange"
    stroke="black"
    stroke-width="3"
  />
</svg>
```

# 渐变

## 线性渐变

<linearGradient> 可用来定义 SVG 的线性渐变, 标签必须嵌套在 <defs> 的内部。

- 标签的 id 属性可为渐变定义一个唯一的名称
- fill:url(#orange_red) 属性把 ellipse 元素链接到此渐变
- x1、x2、y1、y2 属性可定义渐变的开始和结束位置
  - 当 y1 和 y2 相等，而 x1 和 x2 不同时，可创建水平渐变
  - 当 x1 和 x2 相等，而 y1 和 y2 不同时，可创建垂直渐变
  - 当 x1 和 x2 不同，且 y1 和 y2 不同时，可创建角形渐变
- 渐变的颜色范围可由两种或多种颜色组成。每种颜色通过一个 <stop> 标签来规定。offset 属性用来定义渐变的开始和结束位置。

```html
<svg
  width="100%"
  height="100%"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
>
  <defs>
    <linearGradient id="orange_red" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop
        offset="0%"
        style="stop-color:rgb(255,255,0);
            stop-opacity:1"
      />
      <stop
        offset="100%"
        style="stop-color:rgb(255,0,0);
            stop-opacity:1"
      />
    </linearGradient>
  </defs>

  <ellipse cx="200" cy="190" rx="85" ry="55" style="fill:url(#orange_red)" />
</svg>
```

## 放射性渐变

<radialGradient> 用来定义放射性渐变，标签必须嵌套在 <defs> 中

- 标签的 id 属性可为渐变定义一个唯一的名称，
- fill:url(#grey_blue) 属性把 ellipse 元素链接到此渐变，cx、cy 和 r 属性定义外圈，
- fx 和 fy 定义内圈 渐变的颜色范围可由两种或多种颜色组成。
- 每种颜色通过一个 <stop> 标签来规定。offset 属性用来定义渐变的开始和结束位置。

```html
<svg width="100%" height="800" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <radialGradient id="orange-red" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color: rgb(255, 255, 0); stop-opacity: 1" />

      <stop offset="100%" style="stop-color: rgb(255, 0, 0); stop-opacity: 1" />
    </radialGradient>
  </defs>

  <ellipse cx="200" cy="190" rx="85" ry="55" style="fill: url(#orange-red)" />
</svg>
```

# 滤镜

<filter> 标签用来定义 SVG 滤镜，标签必须嵌套在 <defs> 标签内。

- <filter> 标签的 id 属性可为滤镜定义一个唯一的名称（同一滤镜可被文档中的多个元素使用）
- filter:url 属性用来把元素链接到滤镜。当链接滤镜 id 时，必须使用 # 字符
- 滤镜效果是通过 <feGaussianBlur> 标签进行定义的。fe 后缀可用于所有的滤镜
- <feGaussianBlur> 标签的 stdDeviation 属性可定义模糊的程度
- in="SourceGraphic" 这个部分定义了由整个图像创建效果

```html
<svg width="100%" height="600" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <filter id="Gaussian_Blur">
      <feGaussianBlur in="SourceGraphic" stdDeviation="3" />
    </filter>
  </defs>
  <ellipse
    cx="200"
    cy="150"
    rx="70"
    ry="40"
    style="
      fill: indianred;
      stroke: #000000;
      stroke-width: 2;
      filter: url(#Gaussian_Blur);
     "
  />
</svg>
```
