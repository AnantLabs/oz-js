# Examples #

## DOM creation ##
```
var div1 = OZ.DOM.elm("div",{id:"myDiv", "class":"classname", "float":"left", opacity:0.7}); 
var txt = OZ.DOM.text("content"); 
OZ.DOM.append([div1,txt],[document.body,div]);
```

## OOP + Custom events ##
```
var parent = OZ.Class(); 
parent.prototype.log = function(txt) { alert(txt); }; 
parent.prototype.send = function() { 
  this.log("sending event"); 
  this.dispatch("myevent"); 
}; 

var child = OZ.Class(); 
child.extend(parent); 
child.prototype.receive = function(e) { 
  this.log("received event"); 
  OZ.Event.remove(this.event); /* no listening anymore */ 
}; 
child.prototype.init = function(sender) { /* constructor */ 
  this.event = OZ.Event.add(sender, "myevent", this.bind(this.receive)); 
}; 
var sender = new parent(); 
var receiver = new child(sender); 
sender.send(); /* child will respond */
```

## AJAX ##
```
var ajaxOpts = { 
  xml: false,                        /* default = false = text */ 
  method: "post",                    /* default = "get" */ 
  data: "name=value&name2=value2",   /* post data */ 
  headers: {myHeader: "headerValue"} 
}; 
var doSomething = function(data, httpStatus, httpHeaders) { /* process received data and/or statuscode and/or response headers */ }; 
OZ.Request("/someUrl", doSomething, ajaxOpts); 
```