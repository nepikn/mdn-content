---
title: ':autofill'
slug: Web/CSS/:autofill
tags:
  - CSS
  - Pseudo-class
  - Reference
  - Selector
browser-compat: css.selectors.autofill
---
{{CSSRef}}

The **`:autofill`** CSS [pseudo-class](/en-US/docs/Web/CSS/Pseudo-classes) matches when an {{HTMLElement("input")}} element has its value autofilled by the browser. The class stops matching if the user edits the field.

> **Note:** The user agent style sheets of many browsers use `!important` in their `:-webkit-autofill` style declarations, making them non-overrideable by webpages without resorting to JavaScript hacks. For example Chrome has the following in its internal stylesheet:
>
> ```css
> background-color: rgb(232, 240, 254) !important;
> background-image: none !important;
> color: -internal-light-dark(black, white) !important;
> ```
>
> This means that you cannot set the {{cssxref('background-color')}}, {{cssxref('background-image')}}, or {{cssxref('color')}} in your own rules.

## Syntax

```css
:autofill
```

## Examples

The following example demonstrates the use of the `:autofill` pseudo-class to change the border of a text field that has been autocompleted by the browser. For the best browser compatibility use both `:-webkit-autofill` and `:autofill`.

```css
input {
  border: 3px solid grey;
  border-radius: 3px;
}

input:-webkit-autofill {
  border: 3px solid blue;
}
input:autofill {
  border: 3px solid blue;
}
```

```html
<form method="post" action="">
  <label for="email">Email</label> <input type="email" name="email" id="email" autocomplete="email">
</form>
```

{{EmbedLiveSample('Examples')}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Chromium issue 46543: Auto-filled input text box yellow background highlight cannot be turned off!](https://bugs.chromium.org/p/chromium/issues/detail?id=46543)
- [WebKit bug 66032: Allow site authors to override autofilled fields' colors.](https://bugs.webkit.org/show_bug.cgi?id=66032)
- [Mozilla bug 740979: implement `:-moz-autofill` pseudo-class on input elements with an autofilled value](https://bugzilla.mozilla.org/show_bug.cgi?id=740979)
- [new CSS4-UI features - more selectors](https://wiki.csswg.org/spec/css4-ui#more-selectors)
