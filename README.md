# ul-list-menu

## Description

Module for providing a menu object created through composition and including some methods to act on the object

## Installation

Run 'npm install --save-dev ul-list-menu'

## Functions

### makeMenuItems

makeMenuItems(...args: any[])

Creates the unordered list which will be passed as an argument into the function to create the menu. The parameter is an array of strings which contain the text for each li child of the ul.
Returns a ul DOM element with the li elements as children.
Not 

### menuClass

menuClass(listDOMElement)

A function to create the list object with methods attached

```
  const menuClass: (list: any) => {
    addBasicStyling: (key?: string) => void;
    addItem: (value: any, key?: string) => void;
    toggleClass: (class1: any, class2: any, key?: string) => void;
    setTextContent: (oldValue: any, newValue: any, key?: string) => void;
    removeClass: (classToRemove: any, key?: string) => void;
    setClass: (classToSet: any, key?: string) => void;
    attach: (parent?: HTMLElement, child?: string) => void;
    list: any;
  }
```

## Object Methods

Unless otherwise stated, the optional key string is <i>'list'</i>

### addBasicStyling: (key?: string);

Takes an optional argument identifying the key to access the list.
Makes the list a flex column object and removes list style type.

### addItem: (value: any, key?: string);

Adds a new item to the list. Takes two strings as arguments:
1. The text content of the new li.
2. Optional key in string form.

### toggleClass: (class1: any, class2: any, key?: string);

Allows the additonal classes to be toggled on all li elements at once. WTakes 3 arguments:
1. The class to add on first toggle. Removed when class2 is added.
2. The class to add on second toggle. Removed when class1 is readded.
3. Optional key in string form.

### setTextContent: (oldValue: any, newValue: any, key?: string)

Changes the text content of a li elements of the ul. Takes 3 arguments:
1. A string representing the value to be replaced.
2. A string representing the new value.
3. Optional key in string form.

### setClass: (classToSet: any, key?: string)

Adds a class to all li elements of the ul. Takes 2 arguments:
1. A string spcifying the new class.
2. Optional key in string form.

### removeClass: (classToRemove: any, key?: string)

Removes a specified class from all li elements. Takes 2 arguments:
1. A string specifying the class to be removed.
2. Optional key in string form.

### attach: (parent?: HTMLElement, child?: string)

Attaches the ul to a DOM element. Takes 2 optional arguments:
1. An HTML element representing the parent. <em>document.body</em> if not specified.
2. Optional key in string form.
