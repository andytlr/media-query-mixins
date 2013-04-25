Sass @mixins for Less Than and Greater Than Media Queries.

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