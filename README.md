# rapture-stylus

media mixins for stylus

USE:

```stylus
+media-iPad()
  .foo
    font-size 20px
    +media-portrait()
      font-size 22px
  +media-landscape()
    .bar
      font-size 24px
```

will be converted to:

```css
@media screen and (device-width: 768px) and (device-height: 1024px) {
  .foo {
    font-size: 20px;
  }
}
@media screen and (device-width: 768px) and (device-height: 1024px) and (orientation: portrait) {
  .foo {
    font-size: 22px;
  }
}
@media screen and (device-width: 768px) and (device-height: 1024px) and (orientation: landscape) {
  .bar {
    font-size: 24px;
  }
}
```
