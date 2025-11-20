`plawnekjx-load` has been deprecated. You should use [plawnekjx-compile](https://github.com/plawnekjx/plawnekjx-compile).

-----

# plawnekjx-load

Load a Plawnekjx script comprised of one or more Node.js modules.

## Example

```js
var plawnekjx = require('plawnekjx');
var load = require('plawnekjx-load');

load(require.resolve('./agent.js'))
.then(function (source) {
  plawnekjx.attach('Skype')
  .then(function (session) {
    session.createScript(source)
    .then(...) // and so on
  });
});
```

## Installation

```bash
$ npm install plawnekjx-load
```
