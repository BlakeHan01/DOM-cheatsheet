# DOM-cheatsheet

## Structure  
Tree

## Moving Around

- `parentNode`: the node containing the current node

- `childNodes` - an array-like object containing all of the current node's children
  - Has length, no slice() or forEach() or other typical Array methods
- `firstChild` - first child node
- `lastChild` - last child node
- `previousSibling` - previous adjacent node 
- `nextSibling` - next adjacent node

### Siblings
---
#### First Example(without whitespace)
`<img id="b0"><img id="b1"><img id="b2">`   
document.getElementById("b1").previousSibling;    // <img id="b0">    
document.getElementById("b2").previousSibling.id; // "b1"   

#### Second Example(with whitespace)
```
<img id="b0">  
<img id="b1">  
<img id="b2">
```
document.getElementById("b1").previousSibling;                 // #text  
document.getElementById("b1").previousSibling.previousSibling; // <img id="b0">  


## Type of Node example

document.ELEMENT_NODE  
document.TEXT_NODE  
https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeType  

## text content vs inner HTML

example.textContent = '<a href="https://google.com">google</a>';

output: `<a href="http://google.com">google</a>`

example.innerHTML = '<a href="https://google.com">google</a>';

output: <a href="http://google.com">google</a>

