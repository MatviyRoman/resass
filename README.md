# sass-mq-mixin
sass-mq-mixin

@import 'sass-mq-mixin.scss';

<pre>
@include screen(min, max, orientation) {
    //your code
}

@include max-screen(max, orientation) {
    //your code
}

@include min-screen(min, orientation) {
    //your code
}

@include screen-height(min, max, orientation) {
    //your code
}

@include max-screen-height(max, orientation) {
    //your code
}

@include min-screen-height(min, orientation) {
    //your code
}
</pre>
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

Before
<pre>
@include screen(0, 325px) {
    .test {
        width: 100%;
    }
}
</pre>

After
<pre>
@media only screen and (max-width: 325px) {
  .test {
    width: 100%;
  }
}
</pre>
<hr>

Before
<pre>
@include screen(325px) {
    .test {
        width: 100%;
    }
}
</pre>

After
<pre>
@media only screen and (min-width: 325px) {
  .test {
    width: 100%;
  }
}
</pre>
<hr>
Before
<pre>
@include screen-height(100vh, portrait) {
    .test {
        width: 100%;
    }
}
</pre>

After
<pre>
@media only screen and (min-height: 100vh) and (orientation: portrait) {
  .test {
    width: 100%;
  }
}
</pre>
<hr>

Before
<pre>
@include max-screen-height(100vh, landscape) {
    .test {
        width: 100%;
    }
}
</pre>

After
<pre>
@media only screen and (max-height: 100vh) and (orientation: portrait) {
  .test {
    width: 100%;
  }
}
</pre>
