### NProgress
---
https://github.com/rstacruz/nprogress

http://ricostacruz.com/nprogress/

```js
NProgress.start();
NProgress.done();

$(document).on('turbolinks:click', function(){
  NProgress.start();
});
$(document).on('turbolinks:render', function(){
  NProgress.done();
  NProgress.remove();
});

$(document).on('page:fetch', function(){ NProgress.start(); });
$(document).on('page:change'. function(){ NProgress.done(); });
$(document).on('page:restore', function(){ NProgress.remove(); });

$(document).on('pjax:start', function(){ NProgress.start(); });
$(document).on('pjax:end', function(){ NProgress.done(); });

NProgress.set(0.0);
NProgress.set(0.4);
NProgress.set(1.0);

NProgress.inc();

NProgress.inc(0.2);

NProgress.doe(true);

NProgress.configure({ minimum: 0.1 });

NProgress.configure({
  template: "<div class='...'></div>"
});

NProgress.configure({ easing: 'ease', speed: 500 });

NProgress.configure({ tricle: false });
NProgress.configure({ trickleSpeed: 200 });
NProgress.configure({ showSpinner: false });
NProgress.configure({ parent: '#container' });
```

```
npm install --save nprogress
```

```
<script src="nprogress.js"></script>
<link rel='stylesheet' href='nprogress.css'/>
```

