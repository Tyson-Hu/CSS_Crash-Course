# CSS_Crash-Course
继上次HTML5的学习笔记后，一个新的关于CSS3的学习笔记
## 前言
如果你看完上面关于HTML5的速成笔记，那么你会发现你虽然会做一些比较简单的网页但是它们都丑的一批！这也就是为什么一般 `HTML5` 会和 `CSS3` 一起出现的原因。  `HTML` 负责网页出现的元素，而 `CSS` 负责对网页的渲染，让你的网页变得更好看。   

跟上篇 HTML5 的学习笔记一样，这篇文章同样基于 `Leonard Chan` 在 `Youtube` [上传的视频 为初学者准备的：CSS 速成](https://www.youtube.com/watch?v=laEqXy9cjs0&t=6s),在这里非常感谢这位大佬整理出来的速成教程，感激不尽🙏 。如果你也这么觉得，记个点个订阅！（我这算是打广告嘛？？？）

**记住，这仅仅只是我的学习笔记，因此可能只适用我自己，该笔记可能写的比较潦草或者比较片面，但这比较只是 CSS 的速成笔记。讲述的内容也会十分的基础，所以只适用于初学者。作为笔记，我并不会记下所有的东西，我只能保证我自己能看懂即可，如果有任何无法理解的东西，请见谅。**

*这仅仅是我的学习笔记哦，切记不要分享甚至商用！！！（不过我写的这么烂应该没人这么做就是了。。）如果我的学习笔记产生任何版权问题，请即时通知我，我会立刻删除的！*

最后，你可能会问为什么学习笔记不放在你的博客上而是在GitHub上？emmm老实说我也又放在博客上，但是这不打算给博客翻新嘛，到时候给文章搬家太麻烦啦，所以就先放这里咯，顺便也给自己做个备份。（手动滑稽）

## 目录
- 开始之前


## [0]开始之前
- 这是为初学者准备的
- 必须学过 `HTML` 的内容 / 有一定的基础
- 不会涉及 `Flexbox`，`Animation`，`Transition`
- `Keynote` + 示例
- 保持耐心
  
## [1]开始之前需要的准备
- 浏览器
  - Google Chrome
  - Mozilla Firefox
  - Safari
  - Edge
- 编辑器
  - Visual Studio Code
  - Sublime Text
  - Atom
- 即使编辑器
  - codepen.io

## [2]什么是CSS？
- `Cascading Stylesheets` / 层叠样式表
- 与 `HTML` 一样**不是编程语言**
- 用于告诉浏览器如何指定 `样式` 和 `布局` 等等
- 通常与 `HTML`，`XML` 一起工作

## [3]CSS结构
这里我直接使用一个例子来讲解CSS结构：⬇️
```html
<p>Lorem ipsum dolor sit amet</p>  <!--一个段落-->
```
上面这段是HTML，如果想让字变成红色，那么你需要使用CSS来构造：⬇️
```css
p{ /* p为 “Selector / 选择器” */
    color:red; 
}  /* 这里的color为 “Property / 属性” ， red为 “Value / 值” */
   /*注意 red 后面的 “；” ， 一定要加！养成这种习惯！
```
其中这里的 `p` 为 `Selector` 或者 `选择器`。 它就代表着上面 `HTML`里的那个 `p`，在大括号 `{}` 内的所有参数都将运用到这个 `p` 里。`color` 为 `Property` 或者 `属性`，`red` 为 `Value` 或者 `值`，最后在每个参数的结尾都要加一个分号 `；` 以说明该参数到此为止。

## [4]添加CSS
- 外部样式表 
  - `CSS` 保存在 `.css` 文件中
  - 在 `HTML` 里使用 `<link>` 引用
- 内部样式表
  - 不使用外部 `CSS` 文件
  - 将 `CSS` 放在 `HTML` `<style>` 里
- 内敛样式
  - 仅影响一个元素
  - 在 `HTML` 元素的 `style` 属性中添加

### [4-1]具体实例
详情请查看 `CSS` 文件夹里的 `index.html`。
```html
<!-- 外部样式表 -->
<link rel="stylesheet" href="./style.css"> <!-- 切记要先把css与html进行链接！ -->

<!-- 内部样式表 -->
    <style>  /* style 应写在 head 里 */
        h1 {
            color: rgb(0, 255, 255);
        }
    </style>
    .....
    <h1>Hello World!</h1> <!-- h1 应写在 body 里 -->

<!-- 内敛样式 -->
    <h1 style=color: rgb(0, 255, 255)>Hello World!</h>
```
具体效果：   
![4-1-1](image/4-1-1.png)
