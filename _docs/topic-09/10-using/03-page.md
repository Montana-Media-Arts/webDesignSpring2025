---
title: Opacity
module: topic-09
permalink: /topic-09/opacity/
---

<div class="divider-heading"></div>

In addition to setting the color of background elements and text, developers may dictate the **opacity** of elements themselves or just the background color of an element.

Opacity is set as a ratio between 0.0 - 1.0. This controls how much, if at all, elements behind the element in question may be seen. A value of 0.0 would make the element in question _invisible_, and 1.0, make it totally _opaque_.

There are two ways to dictate opacity.


### Background Opacity

You can pass `rgba()` (as opposed to `RGB ()`) to change the opacity of the background color only.

Like, `rgb()`, `rgba()`, takes three numbers to define the ratios of red, green, & blue. However, `rgba()` also take a fourth number, in the range of 0.0-1.0, to define the opacity level.

For example, set a content box to be black at half-opacity:

<div id="code-heading">CSS</div>
```css
.text-box {
    background-color: rgba(0,0,0,0.5);
}
```

### Element Opacity

If the goal is to change the opacity of an entire element, as well as its contents, then you can call the separate `opacity: ` property. Like the fourth argument for `rgba()`, this property takes a single number, between 0.0-1.0, to represent the opacity of an element.

For example, the contents of a container are set at half-opacity:

<div id="code-heading">CSS</div>
```css
div.inner-container {
    opacity: 0.5;
}
```


#### Example

The following example creates 4 elements:

1. `.body-1` is the furthest back with no opacity values set.
2. `.box-1.inner` is nested within box one. The color is set to green, and CSS specifies the `opacity: ` property to be set to 0.5. Notice how both the color of the box, as well as the white text, are affected by the red of `box-1`.
3. `box-2` is a separate element that has been positioned to overlap the other two boxes. Notice that it uses the `rgba()` property, which allows the background color to bleed through, but _NOT_ the text.
4. `image-box` is just a flat, black graphic.


<div class="codepen-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="RwRaOjV" data-default-tab="css,result" data-user="retrog4m3r" data-embed-version="2" data-pen-title="[Topic-07] Opacity" class="codepen"></p>
</div>
