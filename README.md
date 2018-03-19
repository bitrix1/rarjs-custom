[rar.js](https://github.com/43081j/rar.js).

* 
```javascript
		if(typeof Buffer !== 'undefined') {
			var data = [];
			for(var i = offset; i < (offset + length); i++) {
                //Alex
                if(
                    this.getUint8(i) == 0 && this.getUint8(i+1) == 4
                ){
                    // alert('this.getUint8(i) == 0 && this.getUint8(i+1) == 4');
					data = new Uint8Array(data);
					return (new TextDecoder("cp866")).decode(data);
                }
                //Alex
				data.push(this.getUint8(i));
			}
			return (new Buffer(data)).toString();
		}
```