EECoder/Visual Chef Coffeescript Standards
======================

A concise document to help you write quality coffeescript.

* [Layout](#layout)
    * [Spaces](#spaces)
    * [Blank Lines](#blank-lines)
* [Whitespace in Expressions and Statements](#whitespace)
* [Comments](#comments)
    * [Blocks](#blocks)
    * [Inline](#inline)
* [Naming Conventions](#naming-conventions)
* [Module Imports](#module-imports)
* [Selectors](#selectors)

======================

<a name="layout"/>
## Layout

General best practices for all the top level coffeescript development.

<a name="spaces"/>
### Spaces

2 spaces for indents, no tabs.  No whining, this seems to be the way most of the js community does it. :stuck_out_tongue_closed_eyes:

<a name="blank-lines"/>
### Blank Lines

Separate top-level function and class definitions with a single blank line.

```coffeescript
$ ->
  console.log 'time to eat'

class Taco
```

Separate method definitions inside of a class with a single blank line.

```coffeescript
class Taco

  pay: (count)

  eat: (count)
```

Use a single blank line within the bodies of methods or functions in cases where this improves readability (e.g., for the purpose of delineating logical sections).

======================

<a name="whitespace"/>
## Whitespace in Expressions and Statements

__Do Not Add Extra Spaces:__

Immediately inside parentheses, brackets or braces

:-1: __No__
```coffeescript
element: $( ".widget" )
```

:+1: __Yes__
```coffeescript
element: $(".widget")
```

Before commas

:-1: __No__
```coffeescript
noms = (pizza , tacos) ->
```

:+1: __Yes__
```coffeescript
noms = (pizza, tacos) ->
```

Additional recommendations:

- Always surround these binary operators with a **single space** on either side

    - assignment: `=`

        - _Note that this also applies when indicating default parameter value(s) in a function declaration_

        :-1: __No__
        ```coffeescript
           test: (param=null) ->
        ```

        :+1: __Yes__
        ```coffeescript
           test: (param = null) ->
        ```

    - augmented assignment: `+=`, `-=`, etc.
    - comparisons: `==`, `<`, `>`, `<=`, `>=`, `unless`, etc.
    - arithmetic operators: `+`, `-`, `*`, `/`, etc.

    - _(Do not use more than one space around these operators)_

        :-1: __No__
        ```coffeescript
           x      = 1
           y      = 1
           fooBar = 3
        ```

        :+1: __Yes__
        ```coffeescript
           x = 1
           y = 1
           fooBar = 3
        ```

======================

<a name="comments"/>
## Comments

If modifying code that is described by an existing comment, update the comment such that it accurately reflects the new code.

The first word of the comment should be capitalized, unless the first word is an identifier that begins with a lower-case letter.

If a comment is short, the period at the end can be omitted.

<a name="blocks"/>
### Blocks

Block comments apply to the block of code that follows them.

Each line of a block comment starts with a `#` and a single space, and should be indented at the same level of the code that it describes.

Paragraphs inside of block comments are separated by a line containing a single `#`.

```coffeescript
# Below is a seriously complicated function.
# So I'm giving it a really helpful and descriptive
# comment to help myself and others understand.
#
# I'm another paragraph, see how I have an empty line above me.
$ ->
    console.log("I'm actually not that complicated.")
```

<a name="inline"/>
### Inline

Inline comments are placed on the line immediately above the statement that they are describing.

All inline comments should start with a # and a single space.

Do not use inline comments when they state the obvious:

:-1: __No__
```coffeescript
# Increment x
x = x + 1
```

:+1: __Yes__
```coffeescript
# Compensate for border
x = x + 1
```

======================

<a name="naming-conventions"/>
## Naming Conventions

Use `camelCase` (with a leading lowercase character) to name all variables, methods, and object properties.

Use `CamelCase` (with a leading uppercase character) to name all classes.

For constants, use all uppercase with underscores:

```coffeescript
CONSTANT_LIKE_THIS
```

Methods and variables that are intended to be "private" should begin with a leading underscore:

```coffeescript
_privateMethod: ->
```

======================

<a name="module-imports"/>
## Module Imports

If using a module system (CommonJS Modules, AMD, etc.), require statements should be placed on separate lines.

```coffeescript
require 'lib/setup'
Backbone = require 'backbone'
```

These statements should be grouped in the following order:
* Standard library imports (if a standard library exists)
* Third party library imports
* Local imports (imports specific to this application or library)

======================

<a name="selectors"/>
## Selectors

Prefix all javascript-based selectors with js-. This is taken from [http://ozmm.org/posts/slightly_obtrusive_javascript.html](slightly obtrusive javascript).

```
<div class="graphical-selector">I make things pretty and give the site a soul.</div>

<div class="js-functional-selector">I make things work and give the site heart.</div>
```

__Inspired by: [https://github.com/polarmobile/coffeescript-style-guide](Coffeescript-style-guide)__
