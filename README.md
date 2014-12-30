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


####**Selection Nodes by AttributesValues**

Your selection is based on attribute name and/or value. In this case you will be using brackets.

```javascript

$(document).ready(function(){
	$('a[title]').html());
});

```

You are selecting all the ```<a>``` elements that have a title attribute. Or, you can be even more specific:

```javascript

$(document).ready(function(){
	$('a[title="Hello World"]').html());
});

```

In this case you are selecting all the ```<a>``` elements that have a ```"Hello World"``` title as attribute value.

####**Selecting by InputNodes**

For selecting inputs elements like: input, button, image, etc.
This is the basic syntax:

```javascript
$(':input')

```

It selects everything associated with a form.

####**Additional Selector Features**

#####Contains selector


The ```:contains()``` selector searches for matching text.

```javascript

$('div:contains("hello")')
```
In this case we want to select a ```div``` that contains the text ```"hello"```. The contains() search is case-sensitive.

#####Even or Odd Rows in a table selector

The ```$('tr:odd')``` and ```$('tr:even')``` is the jQuery syntax for selecting odd and even rows.

```javascript


```

#####Selecting First Child
This is the syntax for selecting the first-child: ```$('element:first-child')```.

```javascript

$('span:first-child')
``` 
It will search in all the spans and select all the first-child in the spans.


#####Using starts whitin Selectors

If you need to select all the elements with an attribute that __begins__ with a started value, this will be the basic syntax: ```[attribute^="value"]```. Below is an example:

```javascript
$('input[value^="Events"]')
```

And the HTML looks like this:

```html
<input type="button" value="Events-One"/>
```

Above you are selcting any input whose value attribute begins with ```"Events"```. If you want to select all the input that __ends__ with the word ```"Events"``` the code will look like this:

```javascript
$('input[value$="Events"]')

``` 
While, if you just want to select all the input that __contains__ ```"Events"``` in the value attribute, your syntax will look something like:

```javascript
$('input[value*="Events"]')
```

