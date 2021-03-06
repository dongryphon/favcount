# [favcount.js](http://chrishunt.co/favcount)

Enhance your useless favicon with **FavCount&trade;** technology.

[chrishunt.co/favcount](http://chrishunt.co/favcount)

## Usage

Load up `favcount.js` in your HTML.

```html
<html>
  <head>
    <link rel='icon' type='image/png' href='path/to/favicon.ico'>
  </head>

  <body>
    ...
    <!-- bottom of body -->
    <script src='favcount.js' type='text/javascript'></script>
  </body>
</html>
```

Create and use a `Favcount` in your JavaScript.

```javascript
var favicon = new Favcount('path/to/favicon.ico');

favicon.set(10);
```

If you want to make that icon really pop, change it out to something else or
adjust the opacity.

```javascript
favicon.icon = 'path/to/different/icon.ico';
favicon.opacity = 0.5;

favicon.set();
```

## Example

Have a look at the favicon for the [home page](http://chrishunt.co/favcount).
Notice how amazing it is? Here's the code.

```javascript
var favicon = new Favcount('icons/blue-dot.ico');

function setCount(count) {
  if (count > 99) { count = 1 };

  favicon.set(count);

  setTimeout(function() {
    setCount(count + 1);
  }, 500);
}

setCount(1);
```

## License

[MIT License](https://github.com/chrishunt/favcount/blob/master/LICENSE)
