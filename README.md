# JSDOMRect
<br />JSDOMRect Finding X and Y ordinance of element bounding with only visible viewport or current display such also width and height and more...
<br />Source: https://www.w3.org/TR/geometry-1/#DOMRect
<br />Reference: https://javascript.info/coordinates

<br />Detect JSDOMRect properties such X,Y,Top,Bottom by scroll base on browser from end of bookmarks next after seach domain NOT not by scroll bar.
```JS
 // In addition!, Keep in mind that "y" and "top" properties are base on [ browser from end of bookmarks next after seach domain NOT not by scroll bar
 // from the top or begining of element! ] Element that shapes like Rectangle such div, p tag or simply all html tag if we apply style css.
 window.addEventListener("scroll", (event) => {
    let scroll = this.scrollY;
    console.log(scroll)
 });
```

```HTML
<html>
<head></head>
<body id="app-id">
<a id="clickable" href="#">Learn button</a> 
<br />
<br />

<div id="elemTarget">
 <p>Demo Content...</p>
</div>

<script id="app-data">
    
 let btnID    = document.getElementById('clickable');
 let targetID = document.getElementById('elemTarget');

 btnID.addEventListener('click', function(e) {

   let _btnID    = btnID.getBoundingClientRect();
   let _targetID = targetID.getBoundingClientRect();  // the same as : let _targetID = e.target.getBoundingClientRect();
 

    console.log(_btnID);
    console.log('-------------DOM-------------');
    console.log(_targetID);
 
  // Getting Coordinance  X and Y
  console.log(' X : ' + window.pageXOffset + ' Y : ' + window.pageYOffset);
  console.log(' X : ' + document.documentElement.clientWidth + ' Y : ' + document.documentElement.clientHeight);
 
    window.scrollTo({ 
      left: _targetID.left + window.pageXOffset,
      top: _targetID.top + window.pageYOffset,
      behavior : 'smooth'
    }); 

  });

 </script>
</body>
</html>
```

```JS
// Console.log() | Result 
DOMRect {x: 8, y: 8, width: 82.203125, height: 17, top: 8, …}
-------------DOM------------- 
DOMRect {x: 8, y: 186, width: 1350, height: 18, top: 186, …}
 bottom : 204
 height : 18
 left  : 8
 right : 1358
 top : 186
 width : 1350
 x : 8
 y : 186
[[Prototype]] : 
DOMRect
 height : (...)
 width : (...)
 x : (...)
 y : (...)
constructor : ƒ DOMRect()
Symbol(Symbol.toStringTag) : "DOMRect" 
 bottom : (...)
 left : (...)
 right : (...)
 top : (...)
  get height : ƒ height()
  set height : ƒ height()
  get width : ƒ width()
  set width : ƒ width()
  get x : ƒ x()
  set x : ƒ x()
  get y : ƒ y()
  set y : ƒ y()
[[Prototype]] : DOMRectReadOnly
```
