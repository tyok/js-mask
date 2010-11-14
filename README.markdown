js-mask: Give Your JavaScript A Beautiful Mask So It Wouldn't Look Ugly
=======================================================================

A Vim plugin that makes your javascripts look more concise. The original intention is to make anonymous function less verbose and easier to understand at a glance. Requires Vim at least version 7.3.

The functionality can be described in this code below.

Before:
    function Add(b, c) { return b + c; };
    setTimeout(function(){ console.log("wooot") }, 10);

After:
    𝑓 Add(b, c) { return b + c; };
    setTimeout(𝑓(){ console.log("wooot") }, 10);

That's it.

Installation
------------

Put the content of /after folder to ~/.vim folder.

What Does It Do?
----------------

It conceals the "function" keyword.

How Does It Work?
-----------------

You still write the code in normal javascript. This plugin just makes it *looks* concise. It does *not* alter your code. The concealed parts will expand back to normal when you put the cursor at the containing line. Or when you open the code from another editor.

Want to make it even more concise? To hide the text completely, put your Vim into normal mode and type:
    :set cole=3
The author is not responsible for the resulting headache.

To expand *all* concealed text, type:
    :set cole=0

To conceal them back using this plugin settings, type:
    :set cole=2

It Doesn't Do Much!
-------------------

Yes. The main reason is when you move the cursor to a line, all concealed text on that line will expand. I find such behavior quite confusing because texts are moving around. If I had too much concealed keywords then there would be texts flying everywhere everytime I hit 'j' or 'k' and my head would explode.

Feel free to suggest additions and improvements via <https://github.com/tyok/js-mask/issues>. Or you can fork this from <https://github.com/tyok/js-mask> and add your own very personalized flavor.

Credits
-------

This Vim plugin is inspired by <https://github.com/ehamberg/vim-cute-python> which, in turn, is inspired by <http://www.vim.org/scripts/script.php?script_id=3200>.
