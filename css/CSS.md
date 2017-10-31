# CSS 学习笔记

## 基本语法
```bash
.class {
    color: red;
}
#id {
    color: blue;
}
```
## background 背景
* background-color 背景颜色。
* background-image  背景图片。
* background-repeat 设置背景图像是否及如何重复。
* background-attachment 背景图像是否固定或者随着页面的其余部分滚动。
* background-position 设置背景图像的起始位置。

## css 盒子模型
* Margin(外边距) - 清除边框外的区域，外边距是透明的。
* Border(边框) - 围绕在内边距和内容外的边框。
* Padding(内边距) - 清除内容周围的区域，内边距是透明的。
* Content(内容) - 盒子的内容，显示文本和图像。
```bash
div {
    width: 300px;
    border: 25px solid green;
    padding: 25px;
    margin: 25px;
}
```
## 分组嵌套
```bash
h1,h2,p
{
    color:green;
}
```
## 尺寸
* height 设置元素的高度。
* width 设置元素的宽度。
* line-height 设置行高。
* max-height 设置元素的最大高度。
* max-width 设置元素的最大宽度。
* min-height 设置元素的最小高度。
* min-width 设置元素的最小宽度。

## display
<table class="dataintable">
<tbody><tr>
<th>值</th>
<th>描述</th>
</tr>

<tr>
<td>none</td>
<td>此元素不会被显示。</td>
</tr>

<tr>
<td>block</td>
<td>此元素将显示为块级元素，此元素前后会带有换行符。</td>
</tr>

<tr>
<td>inline</td>
<td>默认。此元素会被显示为内联元素，元素前后没有换行符。</td>
</tr>

<tr>
<td>inline-block</td>
<td>行内块元素。（CSS2.1 新增的值）</td>
</tr>

<tr>
<td>list-item</td>
<td>此元素会作为列表显示。</td>
</tr>

<tr>
<td>run-in</td>
<td>此元素会根据上下文作为块级元素或内联元素显示。</td>
</tr>

<tr>
<td>compact</td>
<td>CSS 中有值 compact，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。</td>
</tr>

<tr>
<td>marker</td>
<td>CSS 中有值 marker，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。</td>
</tr>

<tr>
<td>table</td>
<td>此元素会作为块级表格来显示（类似 &lt;table&gt;），表格前后带有换行符。</td>
</tr>

<tr>
<td>inline-table</td>
<td>此元素会作为内联表格来显示（类似 &lt;table&gt;），表格前后没有换行符。</td>
</tr>

<tr>
<td>table-row-group</td>
<td>此元素会作为一个或多个行的分组来显示（类似 &lt;tbody&gt;）。</td>
</tr>

<tr>
<td>table-header-group</td>
<td>此元素会作为一个或多个行的分组来显示（类似 &lt;thead&gt;）。</td>
</tr>

<tr>
<td>table-footer-group</td>
<td>此元素会作为一个或多个行的分组来显示（类似 &lt;tfoot&gt;）。</td>
</tr>

<tr>
<td>table-row</td>
<td>此元素会作为一个表格行显示（类似 &lt;tr&gt;）。</td>
</tr>

<tr>
<td>table-column-group</td>
<td>此元素会作为一个或多个列的分组来显示（类似 &lt;colgroup&gt;）。</td>
</tr>

<tr>
<td>table-column </td>
<td>此元素会作为一个单元格列显示（类似 &lt;col&gt;）</td>
</tr>

<tr>
<td>table-cell</td>
<td>此元素会作为一个表格单元格显示（类似 &lt;td&gt; 和 &lt;th&gt;）</td>
</tr>

<tr>
<td>table-caption</td>
<td>此元素会作为一个表格标题显示（类似 &lt;caption&gt;）</td>
</tr>

<tr>
<td>inherit</td>
<td>规定应该从父元素继承 display 属性的值。</td>
</tr>
</tbody></table>

## position 定位

* static : HTML元素的默认值，即没有定位，元素出现在正常的流中。
           静态定位的元素不会受到 top, bottom, left, right影响。
* fixed : 元素的位置相对于浏览器窗口是固定位置。
          即使窗口是滚动的它也不会移动：
* relative :  相对定位元素的定位是相对其正常位置。

* absolute : 绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>:
    absolute 定位使元素的位置与文档流无关，因此不占据空间。
    absolute 定位的元素和其他元素重叠。
- 重叠元素 使用z-index 设置层级

## float 浮动
* CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。
- 元素的水平方向浮动，意味着元素只能左右移动而不能上下移动。
一个浮动元素会尽量向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。
浮动元素之后的元素将围绕它。
浮动元素之前的元素将不会受到影响。

## 对齐方式

* 文本对齐 : text-align
* 图片居中对齐 : margin: auto
* 左右对齐 : 使用定位方式（absolute） or 使用float方式
* 垂直居中对齐 : 使用padding or 使用line-height or 使用position 和transform
```bash
.center {
    height: 200px;
    position: relative;
    border: 3px solid green;
}

.center p {
    margin: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

## 所有CSS伪类/元素
<table width="100%" cellspacing="0" cellpadding="0" border="1" id="table13" class="reference">
  <tbody><tr>
    <th width="20%" align="left">选择器</th>
    <th width="17%" align="left">示例</th>
    <th width="63%" align="left">示例说明</th>
  </tr>


<tr>
    <td><a href="/cssref/sel-checked.html">:checked</a></td>
    <td>input:checked</td>
    <td>选择所有选中的表单元素</td>
  </tr>
<tr>
    <td><a href="cssref/sel-disabled.html">:disabled</a></td>
    <td>input:disabled</td>
    <td>选择所有禁用的表单元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-empty.html">:empty</a></td>
    <td>p:empty</td>
    <td>选择所有没有子元素的p元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-enable.html">:enabled</a></td>
    <td>input:enabled</td>
    <td>选择所有启用的表单元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-first-of-type.html">:first-of-type</a></td>
    <td>p:first-of-type</td>
    <td>选择每个父元素是p元素的第一个p子元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-in-range.html">:in-range</a></td>
    <td>input:in-range</td>
    <td>选择元素指定范围内的值</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-invalid.html">:invalid</a></td>
    <td>input:invalid</td>
    <td>选择所有无效的元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-last-child.html">:last-child</a></td>
    <td>p:last-child</td>
    <td>选择所有p元素的最后一个子元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-last-of-type.html">:last-of-type</a></td>
    <td>p:last-of-type</td>
    <td>选择每个p元素是其母元素的最后一个p元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-not.html">:not(selector)</a></td>
    <td>:not(p)</td>
    <td>选择所有p以外的元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-nth-child.html">:nth-child(n)</a></td>
    <td>p:nth-child(2)</td>
    <td>选择所有p元素的第二个子元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-nth-last-child.html">:nth-last-child(n)</a></td>
    <td>p:nth-last-child(2)</td>
    <td>选择所有p元素倒数的第二个子元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-nth-last-of-type.html">:nth-last-of-type(n)</a></td>
    <td>p:nth-last-of-type(2)</td>
    <td>选择所有p元素倒数的第二个为p的子元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-nth-of-type.html">:nth-of-type(n)</a></td>
    <td>p:nth-of-type(2)</td>
    <td>选择所有p元素第二个为p的子元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-only-of-type.html">:only-of-type</a></td>
    <td>p:only-of-type</td>
    <td>选择所有仅有一个子元素为p的元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-only-child.html">:only-child</a></td>
    <td>p:only-child</td>
    <td>选择所有仅有一个子元素的p元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-optional.html">:optional</a></td>
    <td>input:optional</td>
    <td>选择没有"required"的元素属性</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-out-of-range.html">:out-of-range</a></td>
    <td>input:out-of-range</td>
    <td>选择指定范围以外的值的元素属性</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-read-only.html">:read-only</a></td>
    <td>input:read-only</td>
    <td>选择只读属性的元素属性</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-read-write.html">:read-write</a></td>
    <td>input:read-write</td>
    <td>选择没有只读属性的元素属性</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-required.html">:required</a></td>
    <td>input:required</td>
    <td>选择有"required"属性指定的元素属性</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-root.html">:root</a></td>
    <td>root</td>
    <td>选择文档的根元素</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-target.html">:target</a></td>
    <td>#news:target</td>
    <td>选择当前活动#news元素(点击URL包含锚的名字)</td>
  </tr>
<tr>
    <td><a href="/cssref/sel-valid.html">:valid</a></td>
    <td>input:valid</td>
    <td>选择所有有效值的属性</td>
  </tr>
  <tr>
    <td><a href="/cssref/sel-link.html">:link</a></td>
    <td>a:link</td>
    <td>选择所有未访问链接</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-visited.html">:visited</a></td>
    <td>a:visited</td>
    <td>选择所有访问过的链接</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-active.html">:active</a></td>
    <td>a:active</td>
    <td>选择正在活动链接</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-hover.html">:hover</a></td>
    <td>a:hover</td>
    <td>把鼠标放在链接上的状态</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-focus.html">:focus</a></td>
    <td>input:focus</td>
    <td>选择元素输入后具有焦点</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-firstletter.html">:first-letter</a></td>
    <td>p:first-letter</td>
    <td>选择每个&lt;p&gt; 元素的第一个字母</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-firstline.html">:first-line</a></td>
    <td>p:first-line</td>
    <td>选择每个&lt;p&gt; 元素的第一行</td>
  </tr>
  <tr>
    <td><a href="/cssref/sel-firstchild.html">:first-child</a></td>
    <td>p:first-child</td>
    <td>选择器匹配属于任意元素的第一个子元素的 &lt;]p&gt; 元素</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-before.html">:before</a></td>
    <td>p:before</td>
    <td>在每个&lt;p&gt;元素之前插入内容</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-after.html">:after</a></td>
    <td>p:after</td>
    <td>在每个&lt;p&gt;元素之后插入内容</td>
  </tr>
	<tr>
    <td><a href="/cssref/sel-lang.html">:lang(<i>language</i>)</a></td>
    <td>p:lang(it)</td>
    <td>为&lt;p&gt;元素的lang属性选择一个开始值</td>
  </tr>
	</tbody></table>