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
