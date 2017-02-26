---
layout: post
title:  "100 Days Of Code: Day 3"
date:   2017-02-25 20:48:24 -0500
categories: 
---
Learned about **code refactoring**: code refactoring is the process of restructuring existing computer code for better readability without changing the behavior (non-functional changes to the code).

Changed in html from this
```
<button id="displayTodos"> Display Todos</button>
```
to this
```
<button onclick="handlers.displayTodos()">Display Todos</button>
```
Changed in js file from this
```
var displayTodosButton = document.getElementById('displayTodosButton');

displayTodosButton.addEventListener('click', function() {
	todoList.displayTodos();
});
```

to this, much shorter and easier to understand
```
var handlers = {
	displayTodos: function() {
	todoList.displayTodos();
}
};
```

"Object is called handlers because we want the methods on this object to handle different events(different clicks) so when the button is clicked we want this object to handle that event. We'll put the methods that handle different events in this object "
\- Gordon Zhu from watchandcode.com
