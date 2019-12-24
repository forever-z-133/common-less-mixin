常见而公用的 less 的 mixin 方法，且只有 mixin 方法，不会产生不必要的 css 导出。

## 1、如何使用

```
npm i -S common-less-mixin
```

```less
// xxx.less
@import '~common-less-mixin';

.someClass {
  .pos-top(); /* 顶部定位 */
  .flex-row(); /* flex 行且水平居中 */
  .child-gap-right(); /* 子元素之间距离为 10px */
  .border-bottom(); /* 底部毛细线 */
}
```

## 2、如何自定义

```less
@px: 1rem;
@import '~common-less-mixin';
```

```less
// 也有打包好的 css 可供使用，但类名会有所不同
@import 'common-less-mixin/dist.css';
```

可配置项一览：
```less
@px: 1rem;

@gap-xs: 5 * @px;
@gap-sm: 10 * @px;
@gap-md: 15 * @px;
@gap-xl: 30 * @px;
@row-gap: @gap-md;
@child-gap: @gap-xs;

@radius-md: 4 * @px;
@radius-round: 1000px;
@radius-circle: 50%;

@border-width: 1 * @px;
@border-color: #e8e8e8;
```

## 3、总览

```less
.border(@color);
.border-top(@color);
.border-left(@color);
.border-right(@color);
.border-bottom(@color);
.raduis(@rdius);
.radius-round();
.radius-circle();

.padding-row(@gap);
.padding-col(@gap);
.margin-row(@gap);
.margin-col(@gap);
.margin-center();
.child-gap-right(@gap);
.child-gap-bottom(@gap);

.flex-row-normal();
.flex-row(@child);
.flex-row-top();
.flex-row-middle();
.flex-row-bottom();
.flex-row-stretch();
.flex-row-left();
.flex-row-center();
.flex-row-right();
.flex-row-wrap();

.flex-col-normal();
.flex-col(@child);
.flex-col-top();
.flex-col-middle();
.flex-col-bottom();
.flex-col-stretch();
.flex-col-left();
.flex-col-center();
.flex-col-right();

.flex-center();

.inblock-row();
.float-row();
.scroller(@dir);
.scroller-x();
.scroller-y();

.input-file();

.cover();
.fit-cover(@fit);
.pos-center();
.pos-top();
.pos-bottom();
.pos-left();
.pos-right();

.text-overflow(@line);
.text-last-justify(@height);

.reset();
.normal-list();
.clearfix();
.rect-box(@width);
.disabled();
.ratio(@ratio);
.image-ratio(@ratio, @fit);
```