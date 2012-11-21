# Web designer's keyboard, θ

Project is closing and migrating to native windows application. There remain only common simple tasks, like color convertor and fake data generator.
Main reasons for this:
– It's difficult to implement nice GUI with Autohotkey. It only suggests simple basic components, which is not very suitable for application's cases. C/C++ will allow to do even Win8 UI.
– Any crossplatform idea is hacked at the root; C/C++ will allow to migrate code.
– Autohotkey swarms with bugs, which is difficult to catch and understand
– It's unusual syntax of autohotkey scripts (something between Pascal, JavaScript and Basic ‽) and difficult debugging of DllCalls

Extend default Windows keyboard with cool typographic tools. Script enables <a href="http://www.nouilles.info/keyboard_shortcuts.html">Mac OS X special characters shortcuts</a>, <a href="http://help.ubuntu.com/community/GtkComposeTable">Linux compose keys</a> premised with <a href="http://docs.oracle.com/cd/E19683-01/806-4743/6jdq6q2n7/index.html">Solaris compose keys</a> and other combinations, easy input of <a href="http://www.w3schools.com/tags/ref_symbols.asp">HTML symbol codes</a>, <a href="http://ilyabirman.ru/projects/typography-layout/">Ilya Birman keyboard layout</a> behaviour, **MS Office**-like autocorrection and other typographic opportunities. Besides, Web Designer's Keyboard℠ supplies a _color convertor_ funciton, that can transform recognized colors in selected sequence of characters to target color format, _get utf code_ function, that can get utf code of selected symbol, _escape_, _string reflect_, _html tags wrapping_, _lorem ipsum generator_.

### TODO:

* Fake address
* Color convertor
* typographic test pages (font, type elements)
* html elements ()
* all possible symbols from utfgraphics
* gethtmlcode, getutf
* readme
* numerous tests
* pr: habrahabr, typographic community, authors of blogs, questions in forums, official forum, mythgol, retrogroup vk, Alex Bur, Korolkova, UTF table idea, Serof Lexa, Wikipedia, get link on script in every comment with (c)…
* rename to the web-designer keyboard, make rgb convertor
* cyrillics full cover & combos & extended
* think & make scenarious: habr image, linux user become windows, etc 
* wikipedia typographic symbols
* a lot of documentation
* make .exe and test autoload (startup)
* fix all bugs
* Make text selected when lorem ipsum generator worked out. It will allow to copy or delete this text


### Ideas:

* rgba to rgb, to hex, to hsl by just select and click hotkey. F.e. select → rgba(25,43,21,.6), hold Alt and strike `rgb`, it will be converted … ? How to define background??? Always mix to the white
* symbol to hmtl notion, like select © → `&copy;`
* phrases, like f.e., …
* Images, like [i:fu] will insert `<img src="link_to_fuuu.png"/>`
* Tags wrapping, for example, selected `phrase` + `AppsKey` + `tag` will wrap text with tag.
* Performs simple actions like *5 (duplicates 5 times)
* Lot of carets, like in sublime text
* Random data generator (like faker)
* Translator?
* ASCII painter?
* Ctrl + left or dblclick = select word correctly
* reverse string (find reversed equivs)
* ms office autocorrection
* escape phrase
* show list of characters balloon
* html escape
* synonims
* omonims
* Symbol suggestions n → (ñ, ň, ń, ǹ, ņ) when type some character with RAlt.
* combos like Entypo & other fonts
* open console here shortcut
* words & symbols counter
* symbols popup 
* duplicate on ctrl+shift+d
* row numbers
* selected string to base64
* show language right on input near caret before input
* data-generator. For example: [list] will generate simple html-list. [list:md] will generate list in markdown syntax. So, [list:wiki] also has sense.
* Microdata-generator
* Fake formats: html, json
* Typograph: format selected text
* any kind of compilers like LESS, SASS, 
* highlighting of invisible symbols, number of spaces etc
* show string enumeration
* zen coding
* toUpperCase
* toLowerCase
* tocamelcase
* mouse slower down (sniper key)
* record actions: start record, stop record, repeat
* code autoformatter
* autosuggestions of tags, data & so on

## Installation
1. Download and install <a href="http://www.autohotkey.com/">Autohotkey</a>™
2. Download <a href="http://dmitry-ivanov.me/playground/windows_typographic_hotkeys/TypographicHotkeys.ahk">TypographicKeyboard.ahk</a>, put it anywhere (i. e. _My Documents_) and open it with Autohotkey™

To make autoloading when windows starts, put it …

## Use Cases

### Inserting characters

There are few ways to insert special characters.

1. **Shortcuts**. Use <a href="http://www.nouilles.info/keyboard_shortcuts.html">OS X shortcuts for special characters</a>, just as if you were using Mac. For example, <kbd>Alt</kbd> + <kbd>-</kbd> = `–`, <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>-</kbd> = `—`, … See <a href="">full list of shortcuts</a>.
2. **Compose Keys**. Symbols are inserted by means of typing some characters while <kbd>Compose Key</kbd> being pressed. <kbd>Compose Key</kbd> is assigned to the <kbd>AltGr</kbd> (the same as <kbd>Right Alt</kbd>). Compose combinations vastly extended to cover a lot more than just Linux/Solaris combinations, see <a href="">full list</a>.
3. **Typing in brackets**. Type sequence in square brackets, and it will be automatically changed to according symbol, if exists one. For example, `[beta]` will be changed to `β`, and `[mdash]`, as well as `[---]` will be changed to `—`. Supports <a href="http://www.w3schools.com/tags/ref_symbols.asp">HTML Symbol Codes</a>, compose key combinations and other sequences (see full list).
4. **Windows characters** method. You can still type keys by `Alt + uCode`. For example, `Alt+0151` will get `—`. Unicode sequences included to combinations, so typing `[0151]` will result the same.

### Autoreplacements

Sequences below will be automatically transformed when typing has finished

 * `(c)` → `©`
 * `(r)` → `®`
 * `...` → `…`

### [pending] Convert color

Transforms found colors in selected string to passed format. For exaple, select `, rgba(25,45,32,.43)`. Hold <kbd>Menu key</kbd>, type rgb and selection will be transformed to [TODO] `, rgb(?,?,?)`. Supported format conversions: rgb, rgba, hsl, hsla, hex, #, plain.
! Supposed that background is white (most common case). Do not use alpha conversion with background other than white.
Nice use case: select all your css, press <kbd>Menu Key + rgb</kbd>, all recognized colors will be converted to `rgb` format. It will enhance rendering of page %)

### [pending] Get code

Html, utf

### [pending] Wrap with tag

Wrap selected with tag

### [pending] Lorem ipsum generator

Text, dif languages, fake data, fake imgs

## Have done
* Densed kbd shortcuts
* Lorem ipsum localisation
* <a href="http://ilyabirman.ru/projects/typography-layout/">Ilya Birman keyboard</a> behaviour
* Lorem Ipsum generator
* Windows <a href="http://en.wikipedia.org/wiki/Alt_code">Alt-codes</a> extended to UTF
* <a href="http://www.nouilles.info/keyboard_shortcuts.html">Mac OSX Shortcuts</a>
* Auto startup
* Linux & Solaris compose keys