Title: DatePicker

DatePicker is a highly configurable widget that adds datepicker functionality to the application. For instance, you can customize the date format, restrict the selectable date ranges, add customized calendar and provide date reference as per your requirement.

The simple way to add DatePicker widget to the application is as follows

<script src='http://snippets.ariatemplates.com/snippets/github.com/ariatemplates/documentation-code/snippets/widgets/datepicker/Snippet.tpl?tag=wgtDatePickerSimple&lang=at&outdent=true'></script>

The whole list of configuration parameters is available in [DatePickerCfg bean](http://ariatemplates.com/api/#aria.widgets.CfgBeans:DatePickerCfg ).

<iframe class='samples' src='http://snippets.ariatemplates.com/samples/github.com/ariatemplates/documentation-code/samples/widgets/datepicker/' ></iframe>

For Instance,you can also add a customized calendar to select the date.

<script src='http://snippets.ariatemplates.com/snippets/github.com/ariatemplates/documentation-code/snippets/widgets/datepicker/Snippet.tpl?tag=wgtDatePickerCustom&lang=at&outdent=true'></script>

<iframe class='samples' src='http://snippets.ariatemplates.com/samples/github.com/ariatemplates/documentation-code/samples/widgets/datepicker/customized/' ></iframe>

## Output of DatePicker with reference

Enter a date in the first date picker and the successive datepickers will take the previously entered date as the reference one when the user input is `+/-N`. If no date is specified then the current date will be taken into account.

<iframe class='samples' src='http://snippets.ariatemplates.com/samples/github.com/ariatemplates/documentation-code/samples/widgets/datepicker/reference/' ></iframe>

## A note about the default DatePicker interface

What follows explains the user experience the clients will get when adding date pickers to an application without whanging their graphical interface.

The calendar view of the DatePicker allows you to do three things:

- navigating throughout the calendar to find the date you want
- selecting the date to insert into the input field
- actually inserting the date

### Navigation

When you open the date picker, the calendar will be centered around the date currently present in the input field, or if none is present around the today date.

You can navigate using your mouse:

- through months by clicking the arrows located at the top corners
- directly to special dates thanks to the links available at the bottom of the date picker:
	- `Today`: centers the calendar around to the current date
	- `Selected date`, available only if a date is actually selected: centers the calendar around to the selected date

You can also navigate using your keyboard (note that this will also whange date selection, see next section):

- through days using the navigation keys
- through months using the `Page Up` and `Page Down` keys: the day in the month will remain the same if possible (all months don't have the same number of days)

### Selection

When you open the date picker:

- if no date is present in the input field, no date is selected
- otherwise, the date corresponding to the one present in the input field is selected

Then, in order to __only__ select a date, use the navigation keys of your keyboard.

### Insertion

To insert a date into the input field, directly click on the day you want.
