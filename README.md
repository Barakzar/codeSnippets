# Convert seconds to hh:mm:ss
```js
function formatSeconds(sec) {
     return [(sec / 3600), ((sec % 3600) / 60), ((sec % 3600) % 60)]
            .map(v => v < 10 ? "0" + parseInt(v) : parseInt(v))
            .filter((i, j) => i !== "00" || j > 0)
            .join(":");
}
```
## Or
```js
d=(s)=>{f=Math.floor;g=(n)=>('00'+n).slice(-2);return f(s/3600)+':'+g(f(s/60)%60)+':'+g(s%60)}
```

# paint items of collection with random colors
```js
function colorCollection(collection) {
    collection.forEach(element => {
        element.style.backgroundColor = `rgba(${Math.round(Math.random()*2*85+85)},
        ${Math.round(Math.random()*2*85+85)},${Math.round(Math.random()*2*85+85)})`
    });
}
```


# 2 dimential array  (rowsCount = first dimention count)
```javascript  
for (i = 0; i < rowsCount -1; i++) { arr[i] = []};
```
