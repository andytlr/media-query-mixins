Sass @mixins for Less Than and Greater Than Media Queries.

## SCSS ##

```scss
.widget {
  height: 300px;
  color: #fff;
  @include ltw(500px) {
    background: red;
    &:before {
      content: 'less than 500px wide';
    }
    @include lth(500px) {
      &:before {
        content: 'less than 500px tall and wide';
      }
    }
  }
  @include gtw(500px) {
    background: blue;
    &:before {
      content: 'greater than 500px wide';
    }
    @include gth(500px) {
      &:before {
        content: 'greater than 500px tall and wide';
      }
    }
  }
}
```

## CSS ##

```css
.widget {
  height: 300px;
  color: #fff;
}
@media only screen and (max-width: 500px) {
  .widget {
    background: red;
  }
  .widget:before {
    content: 'less than 500px wide';
  }
}
@media only screen and (max-width: 500px) and (max-height: 500px) {
  .widget:before {
    content: 'less than 500px tall and wide';
  }
}
@media only screen and (min-width: 500px) {
  .widget {
    background: blue;
  }
  .widget:before {
    content: 'greater than 500px wide';
  }
}
@media only screen and (min-width: 500px) and (min-height: 500px) {
  .widget:before {
    content: 'greater than 500px tall and wide';
  }
}
```