# textfield_datepicker

A collection of three flutter widget [TextfieldDatePicker](https://github.com/joeyyy688/textfield_datepicker/blob/master/lib/src/packages/textfield_datePicker.dart), [TextfieldDateAndTimePicker](https://github.com/joeyyy688/textfield_datepicker/blob/master/lib/src/packages/textfield_dateAndTimePicker.dart) and [TextfieldTimePicker](https://github.com/joeyyy688/textfield_datepicker/blob/master/lib/src/packages/textfield_timePicker.dart).
These widgets gives you access to the various platform date and time pickers based on your device platform. 

The date or time picked is shown in a Material TextFormField widget. 
These three widgets earlier mentioned gives you access to most of Material TextFormField parameters allowing you to design your textfield based on your preference

## Screenshots of how it work


![Image1](https://github.com/joeyyy688/textfield_datePicker_screenshots/blob/main/gif/textfieldDateAndTimePicker(material).gif)

![Image2](https://github.com/joeyyy688/textfield_datePicker_screenshots/blob/main/gif/textfieldDatePicker(ios).gif)

![Image3](https://github.com/joeyyy688/textfield_datePicker_screenshots/blob/main/gif/textfieldDatePicker(material).gif)

![Image4](https://github.com/joeyyy688/textfield_datePicker_screenshots/blob/main/gif/textfieldDateTimePicker(ios).gif)

![Image5](https://github.com/joeyyy688/textfield_datePicker_screenshots/blob/main/gif/textfieldTimePicker(ios).gif)

![Image6](https://github.com/joeyyy688/textfield_datePicker_screenshots/blob/main/gif/textfieldTimePicker(material).gif)



*See [example](https://github.com/joeyyy688/textfield_datepicker/tree/master/example) for details of how this package works*

## Installation

Add the textfield_datepicker package to your `pubspec.yml` file.

```yml
dependencies:
  textfield_datepicker: ^0.0.2
```

Import the package into your dart file

```dart
import 'package:textfield_datepicker/textfield_datepicker.dart';
```

```dart
import 'package:textfield_datepicker/textfield_dateAndTimePicker.dart';
```

```dart
import 'package:textfield_datepicker/textfield_timePicker.dart';
```

## Usage
### TextfieldDatePicker

| Property | Default | Description ||
|---|---|---|---|
|`materialDatePickerInitialEntryMode`|`DatePickerEntryMode.calendar`| In `DatePickerEntryMode.calendar` mode, a calendar grid is displayed and the user taps the day they wish to select. In `DatePickerEntryMode.input` mode a TextField is displayed and the user types in the date they wish to select..|
|`materialDatePickerFirstDate`|`required`| The `materialDatePickerFirstDate` parameter is the earliest allowable date.|
|`materialDatePickerInitialDate`|`required`| When the date picker is first displayed, it will show the month of `materialDatePickerInitialDate`, with `materialDatePickerInitialDate` selected.
|`materialDatePickerLastDate`|`required`| The `materialDatePickerLastDate` parameter is the latest allowable date.|
|`preferredDateFormat`|`required`| The `preferredDateFormat` parameter is for formatting and parsing dates in a locale-sensitive manner.|
|`materialDatePickerBuilder`|optional| The `materialDatePickerBuilder` parameter can be used to wrap the dialog widget to add inherited widgets like Theme.|
|`materialDatePickerLocale`|optional| `materialDatePickerLocale` optional locale argument can be used to set the locale for the date picker. It defaults to the ambient locale provided by Localizations.|
|`materialDatePickerSelectableDayPredicate`|optional| An optional `materialDatePickerSelectableDayPredicate` function can be passed in to only allow certain days for selection.|
|`cupertinoDatePickerMaximumDate`|`required`| The `cupertinoDatePickerMaximumDate` parameter is the maximum selectable date that the picker can settle on.|
|`cupertinoDatePickerMinimumDate`|`required`| The `cupertinoDatePickerMinimumDate` is the minimum selectable date that the picker can settle on.|
|`cupertinoDatePickerMinimumYear`|optional| The `cupertinoDatePickerMinimumYear` parameter is the minimum year that the picker can be scrolled to in CupertinoDatePickerMode.date mode. Defaults to 1 and must not be null.|
|`cupertinoDatePickerMaximumYear`|`required`| The `cupertinoDatePickerMinimumYear` parameter is the minimum year that the picker can be scrolled to in CupertinoDatePickerMode.date mode. Defaults to 1 and must not be null.|
|`cupertinoDatePickerBackgroundColor`|`required`| Defaults to null, which disables background painting entirely. Background color of cupertinoDatePicker.|
|`cupertinoDatePickerKey`|optional| The `cupertinoDatePickerKey` is an identifier.|
|`cupertinoDateInitialDateTime`|`required`| Defaults to the present date and time and must not be null.|
|`cupertinoDateOrder`|optional| Determines the order of the columns inside `CupertinoDatePicker` in date mode. Defaults to the locale's default date format/order.|
|`textfieldDatePickerWidth`|optional| Gives you the option to adjust the width of the `TextfieldDatePicker` widget.|
|`textfieldDatePickerMargin`|optional| Allows you to add some margin to the `TextfieldDatePicker`|
|`textfieldDatePickerPadding`|optional| Allows you to add some padding to the `TextfieldDatePicker`|

```dart
            TextfieldDatePicker(
              cupertinoDatePickerBackgroundColor: Colors.white,
              cupertinoDatePickerMaximumDate: DateTime(2099),
              cupertinoDatePickerMaximumYear: 2099,
              cupertinoDatePickerMinimumYear: DateTime.now().year,
              cupertinoDatePickerMinimumDate: DateTime.now(),
              cupertinoDateInitialDateTime: DateTime.now(),
              materialDatePickerFirstDate: DateTime.now(),
              materialDatePickerInitialDate: DateTime.now(),
              materialDatePickerLastDate: DateTime(2099),
              preferredDateFormat: DateFormat('dd-MMMM-' 'yyyy'),
              textfieldDatePickerController: _controller,
              style: TextStyle(
                fontSize: displayWidth(context) * 0.040,
                fontWeight: FontWeight.w400,
                color: Colors.black,
              ),
              textCapitalization: TextCapitalization.sentences,
              cursorColor: Colors.black,
              decoration: InputDecoration(
                helperStyle: TextStyle(
                    fontSize: displayWidth(context) * 0.031,
                    fontWeight: FontWeight.w700,
                    color: Colors.grey),
                focusedBorder: OutlineInputBorder(
                    borderSide: const BorderSide(color: Colors.white, 
                    width: 0),
                    borderRadius: BorderRadius.circular(2)),
                enabledBorder: OutlineInputBorder(
                    borderRadius: BorderRadius.circular(2),
                    borderSide: const BorderSide(
                      width: 0,
                      color: Colors.white,
                    )),
                hintText: "Select Date",
                hintStyle: TextStyle(
                    fontSize: displayWidth(context) * 0.04,
                    fontWeight: FontWeight.normal),
                filled: true,
                fillColor: Colors.grey[300],
                border: OutlineInputBorder(
                  borderRadius: BorderRadius.circular(10.0),
                ),
              ),
            ),
```

### TextfieldDateAndTimePicker

| Property | Default | Description ||
|---|---|---|---|
|`materialDatePickerInitialEntryMode`|`DatePickerEntryMode.calendar`| In `DatePickerEntryMode.calendar` mode, a calendar grid is displayed and the user taps the day they wish to select. In `DatePickerEntryMode.input` mode a TextField is displayed and the user types in the date they wish to select..|
|`materialDatePickerFirstDate`|`required`| The `materialDatePickerFirstDate` parameter is the earliest allowable date.|
|`materialDatePickerInitialDate`|`required`| When the date picker is first displayed, it will show the month of `materialDatePickerInitialDate`, with `materialDatePickerInitialDate` selected.
|`materialDatePickerLastDate`|`required`| The `materialDatePickerLastDate` parameter is the latest allowable date.|
|`preferredDateFormat`|`required`| The `preferredDateFormat` parameter is for formatting and parsing dates in a locale-sensitive manner.|
|`materialDatePickerBuilder`|optional| The `materialDatePickerBuilder` parameter can be used to wrap the dialog widget to add inherited widgets like Theme.|
|`materialDatePickerLocale`|optional| `materialDatePickerLocale` optional locale argument can be used to set the locale for the date picker. It defaults to the ambient locale provided by Localizations.|
|`materialDatePickerSelectableDayPredicate`|optional| An optional `materialDatePickerSelectableDayPredicate` function can be passed in to only allow certain days for selection.|
|`materialInitialTime`|`required`| When the time picker is first displayed, it will have `materialInitialTime`, as the time selected.|
|`materialTimePickerUse24hrFormat`|optional| Defaults to false.|
|`materialTimePickerInitialEntryMode`|optional| The `materialTimePickerInitialEntryMode` parameter can be used to determine the initial time entry selection of the picker (either a clock dial or text input).|
|`materialTimePickerBuilder`|optional| The `materialTimePickerBuilder` parameter can be used to wrap the dialog widget to add inherited widgets like Localizations.override, Directionality, or MediaQuery.|
|`cupertinoDatePickerMaximumDate`|`required`| The `cupertinoDatePickerMaximumDate` parameter is the maximum selectable date that the picker can settle on.|
|`cupertinoDatePickerMinimumDate`|`required`| The `cupertinoDatePickerMinimumDate` is the minimum selectable date that the picker can settle on.|
|`cupertinoDatePickerMinimumYear`|optional| The `cupertinoDatePickerMinimumYear` parameter is the minimum year that the picker can be scrolled to in CupertinoDatePickerMode.date mode. Defaults to 1 and must not be null.|
|`cupertinoDatePickerMaximumYear`|`required`| The `cupertinoDatePickerMinimumYear` parameter is the minimum year that the picker can be scrolled to in CupertinoDatePickerMode.date mode. Defaults to 1 and must not be null.|
|`cupertinoDatePickerBackgroundColor`|`required`| Defaults to null, which disables background painting entirely. Background color of cupertinoDatePicker.|
|`cupertinoDatePickerKey`|optional| The `cupertinoDatePickerKey` is an identifier.|
|`cupertinoDateInitialDateTime`|`required`| Defaults to the present date and time and must not be null.|
|`cupertinoDateOrder`|optional| Determines the order of the columns inside `CupertinoDatePicker` in date mode. Defaults to the locale's default date format/order.|
|`cupertinoTimePickerUse24hFormat`|optional| Defaults to false.|
|`cupertinoTimePickerMinuteInterval`|optional| The granularity of the minutes spinner, if it is shown in the current mode. Must be an integer factor of 60.|
|`textfieldDateTimePickerWidth`|optional| Gives you the option to adjust the width of the `TextfieldDateAndTimePicker` widget.|
|`textfieldDateTimePickerMargin`|optional| Allows you to add some margin to the `TextfieldDateAndTimePicker`|
|`textfieldDateTimePickerPadding`|optional| Allows you to add some padding to the `TextfieldDateAndTimePicker`|

```dart
            TextfieldDateAndTimePicker(
              cupertinoDatePickerBackgroundColor: Colors.white,
              cupertinoDatePickerMaximumDate: DateTime(2099),
              cupertinoDatePickerMaximumYear: 2099,
              cupertinoDatePickerMinimumYear: 1990,
              cupertinoDatePickerMinimumDate: DateTime(1990),
              cupertinoDateInitialDateTime: DateTime.now(),
              materialDatePickerFirstDate: DateTime.now(),
              materialDatePickerInitialDate: DateTime.now(),
              materialDatePickerLastDate: DateTime(2099),
              preferredDateFormat: DateFormat.yMMMEd(),
              materialTimePickerUse24hrFormat: false,
              cupertinoTimePickerMinuteInterval: 1,
              cupertinoTimePickerUse24hFormat: false,
              textfieldDateAndTimePickerController: _controller,
              style: TextStyle(
                fontSize: displayWidth(context) * 0.040,
                fontWeight: FontWeight.w400,
                color: Colors.black,
              ),
              textCapitalization: TextCapitalization.sentences,
              cursorColor: Colors.black,
              decoration: InputDecoration(
                helperStyle: TextStyle(
                    fontSize: displayWidth(context) * 0.031,
                    fontWeight: FontWeight.w700,
                    color: Colors.grey),
                focusedBorder: OutlineInputBorder(
                    borderSide: const BorderSide(color: Colors.white, 
                    width: 0),
                    borderRadius: BorderRadius.circular(2)),
                enabledBorder: OutlineInputBorder(
                    borderRadius: BorderRadius.circular(2),
                    borderSide: const BorderSide(
                      width: 0,
                      color: Colors.white,
                    )),
                hintText: "Select Date",
                hintStyle: TextStyle(
                    fontSize: displayWidth(context) * 0.04,
                    fontWeight: FontWeight.normal),
                filled: true,
                fillColor: Colors.grey[300],
                border: OutlineInputBorder(
                  borderRadius: BorderRadius.circular(10.0),
                ),
              ),
              materialInitialTime: TimeOfDay.now(),
            ),
```

### TextfieldTimePicker

| Property | Default | Description ||
|---|---|---|---|
|`materialInitialTime`|`required`| When the time picker is first displayed, it will have `materialInitialTime`, as the time selected.|
|`materialTimePickerUse24hrFormat`|optional| Defaults to false.|
|`materialTimePickerInitialEntryMode`|optional| The `materialTimePickerInitialEntryMode` parameter can be used to determine the initial time entry selection of the picker (either a clock dial or text input).|
|`materialTimePickerBuilder`|optional| The `materialTimePickerBuilder` parameter can be used to wrap the dialog widget to add inherited widgets like Localizations.override, Directionality, or MediaQuery.|
|`cupertinoDatePickerBackgroundColor`|`required`| Defaults to null, which disables background painting entirely. Background color of cupertinoDatePicker.|
|`cupertinoDatePickerKey`|optional| The `cupertinoDatePickerKey` is an identifier.|
|`cupertinoDateInitialDateTime`|`required`| Defaults to the present date and time and must not be null.|
|`cupertinoTimePickerUse24hFormat`|optional| Defaults to false.|
|`cupertinoTimePickerMinuteInterval`|optional| The granularity of the minutes spinner, if it is shown in the current mode. Must be an integer factor of 60.|
|`textfieldTimePickerWidth`|optional| Gives you the option to adjust the width of the `TextfieldTimePicker` widget.|
|`textfieldTimePickerMargin`|optional| Allows you to add some margin to the `TextfieldTimePicker`|
|`textfieldTimePickerPadding`|optional| Allows you to add some padding to the `TextfieldTimePicker`|

```dart
            TextfieldTimePicker(
              cupertinoDatePickerBackgroundColor: Colors.white,
              cupertinoDateInitialDateTime: DateTime.now(),
              materialTimePickerUse24hrFormat: false,
              cupertinoTimePickerMinuteInterval: 1,
              cupertinoTimePickerUse24hFormat: false,
              textfieldDateAndTimePickerController: _controller,
              style: TextStyle(
                fontSize: displayWidth(context) * 0.040,
                fontWeight: FontWeight.w400,
                color: Colors.black,
              ),
              textCapitalization: TextCapitalization.sentences,
              cursorColor: Colors.black,
              decoration: InputDecoration(
                helperStyle: TextStyle(
                    fontSize: displayWidth(context) * 0.031,
                    fontWeight: FontWeight.w700,
                    color: Colors.grey),
                focusedBorder: OutlineInputBorder(
                    borderSide: const BorderSide(color: Colors.white, 
                    width: 0),
                    borderRadius: BorderRadius.circular(2)),
                enabledBorder: OutlineInputBorder(
                    borderRadius: BorderRadius.circular(2),
                    borderSide: const BorderSide(
                      width: 0,
                      color: Colors.white,
                    )),
                hintText: "Select Time",
                hintStyle: TextStyle(
                    fontSize: displayWidth(context) * 0.04,
                    fontWeight: FontWeight.normal),
                filled: true,
                fillColor: Colors.grey[300],
                border: OutlineInputBorder(
                  borderRadius: BorderRadius.circular(10.0),
                ),
              ),
              materialInitialTime: TimeOfDay.now(),
            ),
```

## Example

*See the [example](https://github.com/joeyyy688/textfield_datepicker/tree/master/example) for a complete sample app using the various widgets from textfield_datepicker*

### Found an issue or have a suggestion?
<a href="https://github.com/joeyyy688/textfield_datepicker/issues/new/choose" target="_blank"> Create an issue</a>

### Contact
Reach me on Twitter <a href="https://twitter.com/edinjoey" target="_blank">@edinjoey</a>