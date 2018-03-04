# WTF

我是一个 CSS，可以让元素像在 Sketch 里一样对齐父元素。尤其是中间对齐。

假如要让一个叫小明的 dom 和父元素对齐：

````
<爸爸>
  <小明>
````
0. 首先当然要引入本 CSS

1. 给小明的爸爸加 .box

````
<爸爸 class="box">
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
