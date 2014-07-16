# Kangaroo V 1.0

[jQuery](http://jquery.com/) plugin that lets you create beautiful responsive Accordion dropdown content.

```html
<link rel="stylesheet" href="kangaroo.css" />
```

Put the script at the [bottom](https://developer.yahoo.com/performance/rules.html#js_bottom) of your markup right after jQuery:

```html
<script src="jquery.min.js"></script>
<script src="jquery.easing.1.3.js"></script>
<script src="jquery.kangaroo.accordion.js"></script>
```

```html
<ul id="kangaroo">
  <li>
    <a href="#">Title 1</a>
    <div class="kangaroo-content"></div>
  </li>
  <li>
    <a href="#">Title 2</a>
    <div class="kangaroo-content"></div>
  </li>
  <li>
    <a href="#">Title 3</a>
    <div class="kangaroo-content"></div>
  </li>
</ul>
```

Call the [plugin](http://learn.jquery.com/plugins/) function and your carousel is ready.

```javascript
$(document).ready(function(){
  $('#kangaroo').kangaroo();
});
```

## Options
```
  open: -1,
  // if set to true, only one item can be opened. Once one item is opened, any other that is opened will be closed first
  oneOpenedItem: true,
  // speed of the open / close item animation
  speed: 600,
  // easing of the open / close item animation
  easing: 'easeOutCubic',
  // speed of the scroll to action animation
  scrollSpeed: 900,
  // easing of the scroll to action animation
  scrollEasing: 'easeOutCubic',
  // Throttled refresh time
  refreshRate: 500

```

```javascript
$(document).ready(function(){
  $('#kangaroo').kangaroo({
    open: -1,
    oneOpenedItem: true,
    speed: 600,
    easing: 'easeOutCubic',
    scrollSpeed: 900,
    scrollEasing: 'easeOutCubic',
    responsiveClass: false
  });
});
```

## Events

```
 var kangaroo = $('#kangaroo').data('kangaroo');
 kangaroo.openAll();

 $('button').click(function(e){
      var $pouch = $('#kangaroo');
      var $item = $context.find('.pouch');
      kangaroo.close($context, $item);
});

```
```
isOpened - returns true or false
toggleItem($pouch) - opens/closes item
close($pouch, $pouchContent) - closes item
open($pouch, $pouchContent) - opens item
```


## Documentation

None yet

## Contributing

I welcome contributors, bugs, and questions.

### Bug reports

A bug is a **demonstrable problem** that is caused by the code in the repository. Good bug reports are extremely helpful, so thanks!

Guidelines for bug reports:

  1. Use the GitHub issue search — check if the issue has already been reported.

  2. Check if the issue has been fixed — try to reproduce it using the latest `develop` branch in the repository.

  3. Isolate the problem — ideally create a reduced test case and a live example. This [JSFiddle](http://jsfiddle.net/u3FTZ/) is a helpful template you can fork.


**By submitting a patch, you agree to allow the project owner to
license your work under the terms of the [MIT License](LICENSE).**

## License

The code and the documentation are released under the [MIT License](LICENSE).