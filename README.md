[rar.js](https://github.com/43081j/rar.js).

* `DataView.prototype.getString return`
- `data.push(this.getUint8(i));`
+ `return (new TextDecoder("cp866")).decode(data);`