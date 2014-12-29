#**Recap on jQuery**

The following are a series of concise exercises about jQuery


##Part One:

- Selecting Nodes by ID
- Selecting Nodes by ClassName
- Selecting Nodes by AttributeValue
- Selectiong Input Nodes
- Additional Selector Features

####**Selecting Nodes by ID**

Is really easy to select a HTML element with jQuery by using the element's id.

```javascript

$(document).ready(function(){
	$('#elementId').html());
});

```
You can also get different elements via the differnt IDs:

```javascript

$(document).ready(function(){
	$('#firstElementId', '#secondElementId').html());
});

```

####**Selecting Nodes by ClassName**

This selector works as the one above.

```javascript

$(document).ready(function(){
	$('.elementClass').html());
});

```

By selecting class elements, you can for instance change their CSS, as in the example below:

```javascript
$(document).ready(function(){
	$('.firstElementClass', '.secondElementClass').css('background-color', ' green');
});

```
With this jQuery function, you will chenge the background color of ```.firstElementClass``` and ```.secondElementClass``` into green.


