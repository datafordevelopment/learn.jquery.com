---
title:        Use Stylesheets for Changing CSS on Many Elements
level:        intermediate
---

If you're changing the CSS of more than 20 elements using `$.fn.css`, consider
adding a style tag to the page instead for a nearly 60% increase in speed.

```
// fine for up to 20 elements, slow after that
$('a.swedberg').css('color', '#asd123');
$('<style type="text/css">a.swedberg { color : #asd123 }</style>')
    .appendTo('head');
```
