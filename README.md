# scrollable-overlay
A demo of how to prevent body from scrolling when overlay is on, with pure CSS.

### Benefit of This Solution

* Pure CSS
* The content page won't skid to top with overlay on
* Works on Mobile Safari

### HTML Structure

```html
<div class="overlay">
    <div class="overlay-content"></div>
</div>

<div class="background-content">
    lengthy content here
</div>
```
                
### Styling

```css
html, body {
    height: 100%;
}
                
.overlay{
    position: fixed;
    top: 0px;
    left: 0px;
    right: 0px;
    bottom: 0px;
    background-color: rgba(0, 0, 0, 0.8);

    .overlay-content {
        height: 100%;
        overflow: scroll;
    }
}
  
.background-content{
    height: 100%;
    overflow: auto;
}
```

### Compatibility

| Chrome | Safari | Firefox | IE | Mobile Safari
--- | --- | --- | --- | ---
Yes (43.0.2357) |	Yes (8.0.6) |	Yes (38.0.5) |	Partial (!IE8) |	Yes (IOS 8.3)

### Demo

See it in action [here](http://www.luxiyalu.com/playground/overlay/).
