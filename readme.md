# WTF

我是一个 CSS，可以让元素像在 Sketch 里一样对齐父元素。尤其是中间对齐。
20180305 更新：现在还有两种 layout 可以选。呵呵。屌不屌。

# Start

一开始先做点准备工作：

0. 首先当然要引入本 CSS
1. 然后给所有 dom 加上一个 .layer， 这是必须的。你不加也可以，自己看着办。

# 开始用了

## Layout Off

关掉 layout，让儿子像在 Sketch 里一样和爸爸对齐。

````
<爸爸>
  <小明>
````

1. 给爸爸加 .layout-off

	````
	<爸爸 class="layer layout-off">
	  <小明>
	````

2. 给小明自己加以下 class 中的任意一个以达到预期效果（这是 x 轴的，y 轴同理）
  - `.align-x-start` 左对齐
  - `.align-x-end` 右对齐
  - `.align-x-center` 水平中间对齐
  - `.align-x-stretch` 水平两边对齐

3. 给小明加以下属性来调整间距（只在相应的对齐方式下生效）
  - `--l: 2rem` 左边距离为 2rem
  - `--r: 2rem` 右边距离为 2rem
  - `--t: 2rem` 上边距离为 2rem
  - `--b: 2rem` 下边距离为 2rem

4. 设定小明的宽高时，不要用 width, height 了，改成 `--w: 6rem; --h: 6rem` 这样。

会了吗？

## layout stack

这个就是把一群小明排成一列

````
<爸爸>
  <小明>
  <小明>
  <小明>
  <小明>
````

1. 给爸爸加类(效果如何？请自己猜)
	1. `.layout-stack`（必须的）
	1. 设定排列方向（必须的）
		- `.x`
		- `.y`
		- `.xr`
		- `.xr`
	1. 设定小明们如何对齐（可选）
		- `.items-cross-start`
		- `.items-cross-center`
		- `.items-cross-end`
		- `.items-cross-stretch`
	1. 设定小明们在轴上的分布方式（可选）
		- `.items-main-start`
		- `.items-main-center`
		- `.items-main-end`
		- `.items-main-stretch`
		- `.items-main-between`
	1. 设定小明之间的距离（可选，本来是零距离）
		- `gap-s`
		- `gap-m`
		- `gap-l`
2. 给小明加类
	1. `.fit-space` 自动填满爸爸的剩余空间（可选）
	2. 自己决定如何对齐（可选）
		- `.align-start`
		- `.align-center`
		- `.align-end`
		- `.align-stretch`

会了吗？

## layout flow

这个就是把一群小明当做文字一样排成多行。

````
<爸爸>
  <小明>
  <小明>
  <小明>
  <小明>
````

1. 老样子，给爸爸加类(凡是布局，都要同时涉及到爸爸和小明)
	1. `.layout-stack`（必须的）
	1. 设定行的方向（必须的）
		- `.x`
		- `.y`
		- `.xr`
		- `.xr`
	1. 设定小明们如何对齐（可选）
		- `.items-cross-start`
		- `.items-cross-center`
		- `.items-cross-end`
		- `.items-cross-stretch`
	1. 设定小明之间的距离（可选，本来是零距离）
		- `gap-s`
		- `gap-m`
		- `gap-l`
2. 给小明加类
	1. 自己决定如何对齐（可选）
		- `.align-start`
		- `.align-center`
		- `.align-end`
		- `.align-stretch`

会了吗？
