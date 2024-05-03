# 前端八股

### HTML&CSS

#### 1.盒模型相关

它描述了在 HTML 文档中的每个元素都可以看作一个矩形的盒子，这个盒子包含了内容、内边距、边框和外边距四个部分。

1. **内容（Content）**：指的是元素内部的实际内容，比如文本、图片、视频等。内容的大小由元素的宽度（width）和高度（height）属性决定。
  
2. **内边距（Padding）**：内边距是内容与边框之间的空间，它可以使用 CSS 属性 `padding` 来设置。内边距会影响到元素的实际尺寸。
  
3. **边框（Border）**：边框是包围内容和内边距的线条，可以使用 CSS 属性 `border` 来设置。边框有宽度、样式和颜色等属性，可以通过这些属性来定义边框的样式。
  
4. **外边距（Margin）**：外边距是元素与相邻元素之间的空间，可以使用 CSS 属性 `margin` 来设置。外边距会影响到元素与其他元素之间的距离。
  

盒模型分为两种：

- **标准盒模型**：在标准盒模型下，元素的宽度和高度只包括内容的宽度和高度，不包括内边距、边框和外边距。这意味着设置的宽度和高度值仅仅是内容区域的大小。
  
- **IE盒模型**：在IE盒模型下，元素的宽度和高度包括了内容、内边距和边框，但不包括外边距。这意味着设置的宽度和高度值包括了内边距和边框。
  

#### 2.css选择器

当你使用 CSS（层叠样式表）来设计和布局网页时，选择器是用来定位和选择 HTML 元素并为其应用样式的工具。CSS 选择器可以根据元素的标签名、类、ID、属性等多种方式进行选择。

关于`css`属性选择器常用的有：

1. **标签选择器（Type Selector）**：
  
  - 语法：`elementname { styles }`
  - 示例：`p { color: blue; }`
  - 描述：选择所有指定类型的 HTML 元素，并对其应用相同的样式。
2. **类选择器（Class Selector）**：
  
  - 语法：`.classname { styles }`
  - 示例：`.highlight { background-color: yellow; }`
  - 描述：选择具有指定类的所有元素，并对其应用相同的样式。类选择器以 `.` 开头。
3. **ID 选择器（ID Selector）**：
  
  - 语法：`#idname { styles }`
  - 示例：`#header { font-size: 24px; }`
  - 描述：选择具有指定 ID 的单个元素，并对其应用相同的样式。ID 选择器以 `#` 开头。
4. **后代选择器（Descendant Selector）**：
  
  - 语法：`ancestor descendant { styles }`
  - 示例：`div p { color: red; }`
  - 描述：选择所有属于 ancestor 元素后代的 descendant 元素，并对其应用相同的样式。两个选择器之间用空格分隔。
5. **子元素选择器（Child Selector）**：
  
  - 语法：`parent > child { styles }`
  - 示例：`ul > li { list-style-type: circle; }`
  - 描述：选择所有 parent 元素的子元素 child，并对其应用相同的样式。父元素和子元素之间用 `>` 分隔。
  
  后代选择器会选择所有满足条件的后代元素，而子元素选择器只会选择作为父元素直接子元素的元素，不会选择更深层次的后代元素。
  
6. **通用选择器（Universal Selector）**：
  
  - 语法：`* { styles }`
  - 示例：`* { margin: 0; padding: 0; }`
  - 描述：选择所有元素，并对其应用相同的样式。通用选择器用 `*` 表示。
7. **属性选择器（Attribute Selector）**：
  
  - 语法：`[attribute=value] { styles }`
  - 示例：`input[type="text"] { width: 200px; }`
  - 描述：选择具有指定属性值的元素，并对其应用相同的样式。
  

CSS3 中引入了许多新的选择器，这些选择器提供了更强大和灵活的选择元素的方法。以下是一些 CSS3 中新增的选择器：

1. **属性选择器（Attribute Selectors）**：
  
  - `[attribute]`：选择具有指定属性的元素。
  - `[attribute=value]`：选择具有指定属性值的元素。
  - `[attribute~=value]`：选择具有指定属性值的元素，且属性值是以空格分隔的列表中的一个。
  - `[attribute|=value]`：选择具有指定属性值的元素，且属性值是以连字符 `-` 分隔的列表中的一个，或者属性值以该值开头。
  - `[attribute^=value]`：选择具有指定属性值的元素，且属性值以指定值开头。
  - `[attribute$=value]`：选择具有指定属性值的元素，且属性值以指定值结尾。
  - `[attribute*=value]`：选择具有指定属性值的元素，且属性值包含指定的子字符串。
2. **子元素选择器（Child Selectors）**：
  
  - `:first-child`：选择父元素的第一个子元素。
  - `:last-child`：选择父元素的最后一个子元素。
  - `:only-child`：选择父元素中唯一的子元素。
3. **伪元素选择器（Pseudo-elements）**：
  
  - `::before`：在元素内容之前插入生成的内容。
  - `::after`：在元素内容之后插入生成的内容。
  - `::first-line`：选择元素的第一行文本。
  - `::first-letter`：选择元素的第一个字母。
  - `::selection`：选择用户选中的文本。
4. **结构伪类选择器（Structural Pseudo-classes）**：
  
  - `:nth-child()`：选择父元素的第 n 个子元素。
  - `:nth-last-child()`：选择父元素的倒数第 n 个子元素。
  - `:nth-of-type()`：选择具有指定类型的父元素的第 n 个子元素。
  - `:nth-last-of-type()`：选择具有指定类型的父元素的倒数第 n 个子元素。
  - `:not()`：选择不匹配指定选择器的元素。
5. **状态伪类选择器（State Pseudo-classes）**：
  
  - `:checked`：选择被选中的表单元素（如复选框、单选框等）。
  - `:disabled`：选择被禁用的表单元素。
6. **目标伪类选择器（Target Pseudo-classes）**：
  
  - `:target`：选择当前活动的目标元素。

伪类选择器是 CSS 中用于选择元素的一种机制，它允许你根据元素的特定状态或位置来应用样式，而不是根据元素的属性。伪类选择器以 `:` 开头，通常用于选择元素的特定状态或位置。

以下是一些常见的伪类选择器及其应用：

1. **链接伪类（Link Pseudo-classes）**：
  
  - `:link`：选择未被访问的链接。
  - `:visited`：选择已被访问过的链接。
  
  这两个伪类选择器通常用于设置链接的样式，以区分用户访问过的链接和未访问的链接。
  
  示例：
  
  `a:link { color: blue; } a:visited { color: purple; }`
  
2. **用户动作伪类（User Action Pseudo-classes）**：
  
  - `:hover`：选择鼠标悬停在元素上时的状态。
  - `:active`：选择元素被用户激活（例如被点击）时的状态。
  - `:focus`：选择元素获取焦点时的状态。
  
  这些伪类选择器通常用于创建交互式效果，如按钮悬停效果、链接点击效果等。
  
  示例：
  
  `button:hover { background-color: lightblue; } input:focus { border-color: red; }`
  
3. **元素状态伪类（Element State Pseudo-classes）**：
  
  - `:checked`：选择被选中的表单元素（如复选框、单选框等）。
  - `:disabled`：选择被禁用的表单元素。
  
  这些伪类选择器通常用于根据元素的状态来改变样式，如表单中的选中状态或禁用状态。
  
  示例：
  
  `input:checked + label { text-decoration: line-through; } input:disabled { opacity: 0.5; }`
  
4. **结构伪类选择器（Structural Pseudo-classes）**：
  
  - `:first-child`：选择父元素的第一个子元素。
  - `:last-child`：选择父元素的最后一个子元素。
  - `:nth-child(n)`：选择父元素的第 n 个子元素。
  
  这些伪类选择器用于根据元素在文档结构中的位置来选择元素，实现特定的布局效果。
  
  示例：
  
  `li:first-child { font-weight: bold; } p:nth-child(odd) { background-color: lightgray; }`
  

伪元素选择器是 CSS 中一种用于创建虚拟元素并向其应用样式的机制。与伪类选择器不同，伪元素选择器以 `::` 开头，用于向元素的特定部分添加样式，而不是选择元素的状态或位置。

以下是一些常见的伪元素选择器及其应用：

1. **::before**：
  
  - 创建一个在元素内容之前的虚拟元素。
  - 通常用于添加一些额外的内容，比如图标或装饰性的内容。
  
  示例：
  
  `p::before { content: "→ "; color: red; }`
  
2. **::after**：
  
  - 创建一个在元素内容之后的虚拟元素。
  - 通常用于添加一些额外的内容，比如清除浮动、插入文本或图标等。
  
  示例：
  
  `div::after { content: "This is a div element"; font-style: italic; }`
  

选择器优先级：

CSS 优先级是确定样式应用顺序的规则，它决定了当多个样式规则同时应用于同一个元素时，哪一条规则将会被应用。CSS 优先级的计算是基于选择器的特定性（Specificity）的，特定性是一个由四个部分组成的值，决定了样式的优先级。优先级从高到低分别是：

1. **内联样式（Inline Styles）**：应用于 HTML 元素的 `style` 属性中的样式，直接写在 HTML 元素标签中，如：
  
  `<div style="color: red;"></div>`
  
2. **ID 选择器（ID Selectors）**：选择器的特定性为 100，用 `#` 表示，如：
  
  `#header { color: blue; }`
  
3. **类选择器、属性选择器和伪类选择器（Class Selectors, Attribute Selectors, Pseudo-class Selectors）**：选择器的特定性为 10，如：
  
  `.container { background-color: gray; } input[type="text"] { border: 1px solid black; } a:hover { text-decoration: underline; }`
  
4. **元素选择器和伪元素选择器（Element Selectors, Pseudo-element Selectors）**：选择器的特定性为 1，如：
  

**注意事项：**

- !important声明的样式的优先级最高；
- 如果优先级相同，则最后出现的样式生效；
- 继承得到的样式的优先级最低；
- 通用选择器（*）、子选择器（>）和相邻同胞选择器（+）并不在这四个等级中，所以它们的权值都为 0 ；
- 样式表的来源不同时，优先级顺序为：内联样式 > 内部样式 > 外部样式 > 浏览器用户自定义样式 > 浏览器默认样式。

#### 3.css单位：em/px/rem/vh/vw

传统的项目开发中，我们只会用到`px`、`%`、`em`这几个单位，它可以适用于大部分的项目开发，且拥有比较良好的兼容性

从`CSS3`开始，浏览器对计量单位的支持又提升到了另外一个境界，新增了`rem`、`vh`、`vw`、`vm`等一些新的计量单位

利用这些新的单位开发出比较良好的响应式页面，适应多种不同分辨率的终端，包括移动设备等。

在`css`单位中，可以分为长度单位、绝对单位，如下表所指示

| CSS单位 |     |
| --- | --- |
| 相对长度单位 | em、ex、ch、rem、vw、vh、vmin、vmax、% |
| 绝对长度单位 | cm、mm、in、px、pt、pc |

这里我们主要讲述px、em、rem、vh、vw
