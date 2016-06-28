# Ember-flatpickr

<a href="http://shipshape.io/"><img src="http://i.imgur.com/EVjM7AV.png" width="100" height="100"/></a>

[![Ember Observer Score](https://emberobserver.com/badges/ember-flatpickr.svg)](https://emberobserver.com/addons/ember-flatpickr)
[![Build Status](https://travis-ci.org/shipshapecode/ember-flatpickr.svg?branch=master)](https://travis-ci.org/shipshapecode/ember-flatpickr)
[![Code Climate](https://codeclimate.com/github/shipshapecode/ember-flatpickr/badges/gpa.svg)](https://codeclimate.com/github/shipshapecode/ember-flatpickr)
[![Test Coverage](https://codeclimate.com/github/shipshapecode/ember-flatpickr/badges/coverage.svg)](https://codeclimate.com/github/shipshapecode/ember-flatpickr/coverage)

This is an Ember addon that wraps the date picker [Flatpickr](http://chmln.github.io/flatpickr/). I wanted to use npm instead of bower, so ember-browserify is also required to get this working.

## Demo

[![Guide your users through a tour of your app](http://i.imgur.com/9ZvagVn.png)](http://shipshapecode.github.io/ember-flatpickr/)
http://shipshapecode.github.io/ember-flatpickr/

## Installation

`npm i -D flatpickr ember-browserify`

`ember install ember-flatpickr`

## Usage

```hbs
{{ember-flatpickr
altFormat="Y-m-d"
altInput=true
dateFormat="M/D/Y"
defaultDate=defaultDate
disable=datesToDisable
enableTime=true
hourIncrement=1
inline=false
maxDate=maxDate
minDate=minDate
minuteIncrement=5
noCalendar=false
onChangeAction="doSomeStuffOnChange"
onCloseAction="doSomeStuffOnClose"
parseDate=false
placeholder="Choose a Date"
timeFormat="H:i"
time_24hr=false
value=(mut dateValue)}}
```

*(All options are displayed, but they have defaults and you only need to pass what you need)

*Note:* If you want the value to update when you select a date, and `onChange` fires, you have to use the `mut` helper.

Whenever a new date is selected, `onChange` will set the value to the newly selected date. It will also fire the action `onChangeAction`, and pass the new `dateObject` to that action.This allows you to pass whatever action you may want in to happen on change.

## Observers

`maxDate` and `minDate` are watched by observers, and will update the flatpickr instance whenever you change them. This allows you to do things like having two components, used as a range picker, and updating the `minDate` and `maxDate` to display valid date choices on each.

## Options

All options available to Flatpickr are available here. 

Please see the [flatpickr docs](https://chmln.github.io/flatpickr/) for a full list of options.

## Contributing

If there are features you would like to see implemented, or we have missed some flatpickr options, please open an issue and/or submit a PR!


