tolerant url-parser [![Build Status](https://drone.io/github.com/FGRibreau/node-tolerant-url-parser/status.png)](https://drone.io/github.com/FGRibreau/node-tolerant-url-parser/latest) [![Gittip](http://badgr.co/gittip/fgribreau.png)](https://www.gittip.com/fgribreau/) [![Deps](https://david-dm.org/FGRibreau/node-tolerant-url-parser.png)](https://david-dm.org/FGRibreau/node-tolerant-url-parser)
========================

Overly tolerant url parser specialized in parsing protocol, auth (even invalid ones), host and port url parts.

[![npm](https://nodei.co/npm/tolerant.png)](https://npmjs.org/package/tolerant)

### Usage

```javascript
var TolerantUrl = require('tolerant');

console.log(TolerantUrl.parse('protocol://user:auth@domain.com:port'));

// should print
{
  'protocol': 'protocol:',
  'auth': 'user:auth',
  'hostname': 'domain.com',
  'host': 'domain.com:port',
  'port': 'port',
  'href': 'protocol://user:auth@domain.com:port'
}

// and that's all.
```

Check `test/main.js` for examples of weird urls parsed by `tolerant`.


### License

Copyright (c) 2014, Francois-Guillaume Ribreau node@fgribreau.com.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
