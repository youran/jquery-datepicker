

## Datepicker

**Element HTML:**
```html
<!-- Default HTML -->
<div class="jquery-datepicker">
    <label>[Text Only]</label>
    <input type="text" class="jquery-datepicker__input">
</div>

<!-- HTML with attributes -->
<div class="jquery-datepicker" data-selected-date="[parameter]" data-start-date="[parameter]" data-end-date="[parameter]" data-format="[parameter]">
    <label>[Text Only]</label>
    <input type="text" class="jquery-datepicker__input">
</div>
```


**Javascript**
```html
$('.jquery-datepicker').datepicker();
```
### Attributes
Attributes are used to pass parameters to datepicker's initialization function.
Attributes must set in the same element which has class `jquery-datepicker` to function correctly.

| Name | Description | Possible Values | Default Value |
| ---- | ------ | ----------- | -------- |
| data-selected-date | Set the selected date | Three types of value are accepted:<br />a) "YYYY-M-D": such as "2017-3-8"<br />b) "-Nd" or "+Nd": where N is the days prior or posterior to today. e.g., "+3d"<br />c) "none": if "none" is specifed, no date will be selected on initialization | If not set, today will be selected |
| data-start-date | Set the first day (included) of selectable dates. Dates prior to this date will be grayed out and not selectable | Refer to a), b) of above | If not set, every day is selectable |
| data-end-date | Set the last day (included) of selectable dates. Dates posterior to this date will be grayed out and not selectable | Refer to a), b) of above | If not set, every day is selectable |
| data-format | Set the date format to be displayed on the input field | "yyyymmdd"<br />"ddmmyy"<br />"mmddyyyy"<br />"yymmdd"<br />"ddmmyy"<br />"mmddyy" | If not set, date format is "ddmmyy", e.g., "24/05/17" |

### APIs
Two APIs are provided to get/set Date object from datepicker.

| Name | Example | Explanation |
| -------- | ----------- | --------- |
| set | $('.jquery-datepicker').datepicker('set', DateObject); | Set the current selected date.<br />DateObject must be a valid javascript Date object or null.<br />If DateObject is null, the datepicker will be set to no date selected.<br /> This will apply to all datepickers matched by jquery. |
| get | DateObject = $('.jquery-datepicker').datepicker('get'); | Get a Date object for currently selected date. If no date is selected, the API will return null. <br /> This API is intended to be applied to a single datepicker, so make sure only one is selected by jquery. |
