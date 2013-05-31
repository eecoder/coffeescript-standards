EECodeer/Visual Chef Coffeescript Standards
======================

A concise document to help you write quality coffeescript.

## Comments

If modifying code that is described by an existing comment, update the comment such that it accurately reflects the new code.

The first word of the comment should be capitalized, unless the first word is an identifier that begins with a lower-case letter.

If a comment is short, the period at the end can be omitted.

### Blocks

Block comments apply to the block of code that follows them.

Each line of a block comment starts with a `#` and a single space, and should be indented at the same level of the code that it describes.

Paragraphs inside of block comments are separated by a line containing a single `#`.

```
# Below is a seriously complicated function.
# So I'm giving it a really helpful and descriptive
# comment to help myself and others understand.
#
# I'm another paragraph, see how I have an empty line above me.
$ ->
    console.log("I'm actually not that complicated.")
```

======================

## Selectors

Try to prefix all javascript-based selectors with js-. This is taken from [http://ozmm.org/posts/slightly_obtrusive_javascript.html](slightly obtrusive javascript). The idea is that you should be able to tell a presentational class from a functional class. Most of the codebase doesn't do this, let's try and move toward it.

__Inspired by: [https://github.com/polarmobile/coffeescript-style-guide](Coffeescript-style-guide)__
