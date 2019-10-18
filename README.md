# Convert seconds to hh:mm:ss
```js
function formatSeconds(sec) {
     return [(sec / 3600), ((sec % 3600) / 60), ((sec % 3600) % 60)]
            .map(v => v < 10 ? "0" + parseInt(v) : parseInt(v))
            .filter((i, j) => i !== "00" || j > 0)
            .join(":");
}
```
#### Or
```js
d=(s)=>{f=Math.floor;g=(n)=>('00'+n).slice(-2);return f(s/3600)+':'+g(f(s/60)%60)+':'+g(s%60)}
```

```javascript
parseInt(getComputedStyle(div).border)
```

# Paint items of collection with random colors
```js
function colorCollection(collection) {
    collection.forEach(element => {
        element.style.backgroundColor = `rgba(${Math.round(Math.random()*2*85+85)},
        ${Math.round(Math.random()*2*85+85)},${Math.round(Math.random()*2*85+85)})`
    });
}
```
#### Or (create a random color)
```
div.style.background = '#' + Math.random().toString(16).slice(-6)
```



# Two dimential array  (rowsCount = first dimention count)
```javascript  
for (i = 0; i < rowsCount -1; i++) { arr[i] = []};
```

# Find  width / height / coordinations
```javascript
div.getBoundingClientRect() // Relativ to the window  x = left, y = top, bottom = top+height, right = left+width.
div.getBoundingClientRect() + pageXOffset//pageYOffset   //Relativ to the document/
document.elementFromPoint(x, y)  // Return the most nested element in window cordinate(x, y)

div.clientHeight / div.clientWidth // Height / width of the element (without border)
div.clientLeft / div.clientTop // width of the border.

div.offsetHeight / div.offsetWidth // height / width of the element (with border !)
div.offsetLeft / div.offsetTop // Distance from top/left of the --div.offsetparent--.
```
# css - create tappet by repeating-radial-gradient and border
```css
div {
    width: 20px;
    height: 20px;
    background-image: repeating-radial-gradient(red,red 3px,darkred 3px, darkred 6px); 
    border: 40px solid transparent;
}
```
