# sass-media-queries-mixin
sass-media-queries-mixin

@import 'sass-queries-mixin.scss';

@include screen(min, max, orientation) {
    //your code
}
<hr>


Before
<pre>
@include screen(320px, 768px, portrait) {
    .test {
        width: 100%;
    }
}
</pre>

After
<pre>
@media only screen and (max-width: 768px) and (min-width: 320px) and (orientation: portrait) {
  .test {
    width: 100%;
  }
}
</pre>
<hr>

Before
<pre>
@include screen(768px, 320px, landscape) {
    .test {
        width: 100%;
    }
}
</pre>

After
<pre>
@media only screen and (max-width: 768px) and (min-width: 320px) and (orientation: landscape) {
  .test {
    width: 100%;
  }
}
</pre>
<hr>
