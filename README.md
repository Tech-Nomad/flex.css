# About 
A collection of Flexbox CSS rules / prefixes using the LESS pre-processor which allows you to achieve around 99% coverage of all browsers used today including IE 11, Android 4.4 and iOS 7.1

  
## Usage in HTML
```html
<ul class="display-flex flex-column align-items-center">
   <li></li>    
   <li></li>    
   <li></li>
</ul>
```

## Usage in .less files
It allows you to avoid repetitive declaration by assigning all usages of this mixins in your project to one single declaration block (for each flex rule extender) 
```css
#someID{
  .displayFlexExtender();
  .flexColumnExtender();
  .alignItemsCenterExtender();
}   
```

## Usage without LESS
If you just want to use it without LESS, then you just need to include the flex.css file in your HTML document.

## :extend inside medie queries
Unfortunatly you can't use the extender mixins within media queries like this:

```css
.some-class{
    .displayFlexExtender();
}

@media (max-width: 767px){
    .some-class{
        .displayFlexExtender();
    }
}
```

The rules will be ignored. For more information see:

[http://lesscss.org/features/#extend-feature-scoping-extend-inside-media](http://lesscss.org/features/#extend-feature-scoping-extend-inside-media)

[https://github.com/less/less.js/issues/1165](https://github.com/less/less.js/issues/1165)

[https://stackoverflow.com/questions/30375305/less-css-extend-and-media-queries](https://stackoverflow.com/questions/30375305/less-css-extend-and-media-queries)


Instead you can use the mixins without :extend e.g.:


```css
.some-class{
    .displayFlexExtender;
}

@media (max-width: 767px){
    .some-class{
        .displayFlex;
    }
}
```

Yes, this will cause repetitive declarations. But after applying this workoraund on my recent project the app size has increased only by 1kb more. Whereas the extenders used outside any media queries have reduced the app size by 20kb. 
