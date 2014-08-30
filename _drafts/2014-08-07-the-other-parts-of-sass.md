---
layout: post
title: "The Other Parts of SASS"
categories:
- SASS
date: 2014-08-07 10:14:43
---

If you write SASS there's a chance you're only seeing the tip of the iceberg. Most times when I write SASS everyday, I use [imports](http://sass-lang.com/guide#topic-5), [nesting](http://sass-lang.com/guide#topic-3) and [variables](http://sass-lang.com/guide#topic-2) then less often mixins and extends. All makes authoring stylesheets incredibly easier, but that's not all of what SASS can do, hell that's not even close.

### Basic Operators

You can make your SASS files do some basic math for you.

<pre><code class="language-scss">$baseFontSize: 100%;
.main--content {
    width: 100% * .75;
}
.sidebar {
    width: 100% * .25;
    h3 {
        font-size: $baseFontSize - .25;
    }
}</code></pre>

That will totally compile into that for you:

<pre><code class="language-css">.main--content {
  width: 75%;
}

.sidebar {
  width: 25%;
}
.sidebar h3 {
  font-size: 88.88889%;
}
</code></pre>

That's pretty useful. But there's still way more.

### Content Directive

[for keyframes](https://gist.github.com/ericam/1607696)

[for media queries](http://thesassway.com/intermediate/responsive-web-design-in-sass-using-media-queries-in-sass-32)