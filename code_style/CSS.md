## CSS 方法论

### OOCSS (Object Oriented CSS)

面向对象的 CSS，是由 Nicole Sullivan 提出的 css 理论，两个主要的原则是：

1. 分离结构（structure）和主题（skin）：分离结构和主题是将视觉样式效果（background、color）作为单独的主题采用，阴影效果单独写在 `.media-shadow` 的 class 里，成为可选择、可拆分的主题。
2. 分离容器（container）和内容（content）

```
<div class="media media-shadow">
    <div class="media-image-container">
        <img class="media-image" src="rean.jpg" alt="">
    </div>
    <div class="media-body">
        <p class="media-text">本作的主角，帝国北部地方贵族施瓦泽男爵的养子，也是托尔兹士官学校特科班“Ⅶ组”的成员。</p>
    </div>
</div>

.media{
    padding: 10px;
}
.media:after{
    display: table;
    clear: both;
    content: " ";
}
.media-image-container{
    float: left;
    margin-right: 10px;
}
.media-image{
    display: block;
}
.media-body{
    overflow: hidden;
}
.media-shadow{
    box-shadow: 1px 1px 3px rgba(0, 0, 0, .5);
}
```
