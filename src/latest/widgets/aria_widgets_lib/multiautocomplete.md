Title: MultiAutoComplete

TODO Highlighted mode is explained after

## Navigation

The user can navigate inside the widget.

However, this is a complex widget with different kinds of elements. To summarize, there are two main elements, located one after the other:

* the list of selected options
* the text input field

It is then possible to navigate inside one of these elements, but also between those elements, passsing from one to the other.

### In input field

Navigation inside the text input field is not changed from its default.

However there are two particular things to be noted:

* pressing the tab key gives focus to the next focusable element on the page (leaving the widget)
* navigating to the left — with the left arrow key in this case — when the caret is at the beginning of the input field enters the highlighted mode, highlighting the last option. The latter applies only when there is actually at least one selected option.

### Through list of selected options

Navigation inside the list of selected option is related to the concept of the highlighted mode. Navigating in this case means highlighting either the previous (left) or next (right) option. Respectively the left and right arrow keys are used for that.

In this context, pressing the tab key leaves the highlighted mode, giving focus to the input field, with the caret at the beginning.


----

WRONG Tab is used for right navigation between containers


## Navigation

### Concepts

We'll talk about navigating to the right and to the left, no matter which keys are actually used. Which ones can be used depends on the context and will be mentioned when appropriate.

We don't change the behavior for navigation __inside__ a text value. __Here our text value corresponds to the input field.__

For navigation of the selection of custom items, navigating _to the left_ means selecting the previous items while _to the right_ means the next one. It doesn't matter how items visually appear in the widget. __Here our custom items correspond to the selected options.__

An important thing regarding what has been told: the list of selected options is located before the input field.

### Navigation contexts/states

There are two contexts of navigation:

* inside the input field: the edit mode
* through the currently selected options: the highlighted mode

When there is no selected option at all, the state remains the edit mode, even if there is no current value.

----

* when the caret is at the beginning of the input field, it is at the edge of the last selected option
* when the widget is in highlighted mode and the last selected option is highlighted, it is at the edge of the input field

When the position is at the edge of a container, navigation towards the other container exits the first one, with all the implications behind, and enters the second one.

### In input field

_As told before, the navigation inside the text-based input field is not changed._

The only thing is when the caret is at the begining of the field: in this case, it is at the edge of the selected options list, and more precisely of the last option. Thus, navigating to the left enters the highlighted mode with the last option highlighted.

### In selected options list

In this state, as told before navigating to the left and the right changes the highlighted item, respectoively selecting the previous one or the next one, __when available__.

If there is no previous item, navigating to the left does nothing.

When the last option is highlighted, there is no follsing option, however teh following element is teh input field. This way, navigating to teh right goes to the input field.

Here are the keys that can be used for navigation in this context:

* right: right arrow, tab
* left: left arrow
