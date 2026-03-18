Markdown, Humanized
===================

**A More Pleasant Way to Print & View Markdown.**

The site is now live [here](http://markdowner.github.io)!

This site is an afternoon hack to fill a need of my own: the ability to print and view markdown in a appealing and typographically tasteful manner. This isn’t something most markdown apps are good at.

**Take a look at TODO.md to see where this project is headed.**

![Screenshot 1](http://markdowner.github.io/img/markdown-humanized.png)
![Screenshot 2](http://markdowner.github.io/img/markdown-humanized-2.png)

## Fork Notes

**Print Fix: Code Block Line Height**

The original project has a bug where code blocks overlap when printed — each line covers part of the line above it. This is caused by the browser substituting fonts at print time, which causes the effective line height to collapse.

This fork fixes it by adding explicit print styles for `pre` and `code` blocks in `css/style.css`:

```css
@media print {
  pre, code {
    line-height: 1.5 !important;
    white-space: pre-wrap;
    page-break-inside: avoid;
  }
}
```

