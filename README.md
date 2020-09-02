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

# 滤镜

# 渐变
