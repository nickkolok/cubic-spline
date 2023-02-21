## Disclaimer

This library is a fork of [cubic-spline](https://www.npmjs.com/package/cubic-spline).
The only intent of the fork is to get the library work in a browser out-of-the-box.
A [pull request](https://github.com/morganherlocker/cubic-spline/pull/19) has been sent to upstream;
if and when it is merged, you will perhaps prefer the upstream version.


# cubic-spline

A slight modification of [Ivan Kuckir's cubic spline implementation](http://blog.ivank.net/interpolation-with-cubic-splines.html), cubic-spline guesses the value of y for any x value on a line. This is helpful for smoothing line graphs.

## installation

```sh
npm install cubic-spline-browserified
```

## usage

```js
const Spline = require('cubic-spline-browserified'); // Still works

const xs = [1, 2, 3, 4, 5];
const ys = [9, 3, 6, 2, 4];

// new a Spline object
const spline = new Spline(xs, ys);

// get Y at arbitrary X
console.log(spline.at(1.4));

// interpolate a line at a higher resolution
for (let i = 0; i < 50; i++) {
  console.log(spline.at(i * 0.1));
}
```

or

```html
<script src="node_modules/cubic-spline-browserified/cubic-spline-for-browser.js"></script>
<script>
	const xs = [1, 2, 3, 4, 5];
	const ys = [9, 3, 6, 2, 4];
	const spline = new Spline(xs, ys);
	// ...
</script>
```


## test

```sh
npm test
```

## lint

```sh
npm run lint
```
