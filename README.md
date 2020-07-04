# JavaScript Deferred Promise

A copy-paste friendly implementation of the deferred promise pattern ready for
you to use, because this pattern is useful no matter what others may tell you.

```js
export default class Deferred extends Promise {
  constructor() {
    let _resolve;
    let _reject;
    super((resolve, reject) => {
      _resolve = resolve;
      _reject = reject;
    });

    this.resolve = _resolve;
    this.reject = _reject;
  }
}

Deferred.prototype.constructor = Promise;
```

https://stackoverflow.com/a/48159603/2715716
