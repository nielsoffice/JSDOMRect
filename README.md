# JSDOMRect
JSDOMRect Finding X and Y ordinance of element bounding with only visible viewport or current display such also width and height and more... ... 


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
   let _targetID = targetID.getBoundingClientRect();

    console.log(_btnID);
    console.log('-------------DOM-------------');
    console.log(_targetID);

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
