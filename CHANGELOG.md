# Changelog

## 1.0.8 (current)
* JS now checks to make sure the editor is enabled before trying to replace it with the Ace editor.

### 1.0.7
* Replaced `ParsedownExtra` with an extension that removes support for indent-triggered code blocks. Previously, this feature of the Markdown specification would cause shortcode-generated HTML to be interpreted as a code block.

### 1.0.6
* Fixed image sizing when using the shortcode.

### 1.0.5
* Adjusted image shortcode to use better figure classes.
* Removed ID attributes from both the `figure` and `img` so it's possible to use the same image twice on one page.
* Removed a bunch of leftover files from early releases.

### 1.0.4
* Yes, I had to create a hotfix for not incrementing the version number of my last hotfix. Leave me alone.

### 1.0.3
_Well, that didn't take long._

* Replaced the quote unescaper with a filter to add `markdown="1"	` to block-level elements, taking advantage of [Markdown Extra's ability](https://michelf.ca/projects/php-markdown/extra/#markdown-attr) to handle nested formatting natively.
* Adjusted filter priorities _again_

### 1.0.2
* Adjusted filter priorities to make sure Markdown parsing is done at the correct point in the filter chain.
* Added an additional filter to unescape quotes in shortcode definitions, since shortcodes must be processed _after_ parsing. 
* Refactored image shortcode.

### 1.0.1
* Removed a duplicate submit binding in the editor JS that was causing post previews to fail.

### 1.0.0
* Added composer support and majorly refined codebase
* Now uses the [Ace](https://ace.c9.io/#nav=about) editor for more Markdown-friendly editing
* **Removed** the live preview meta box; it'll be back soon!

### 0.5.3

* Switched to using a character limit (16k characters) instead of time limit

### 0.5.2

* Added a timeout to the previewer AJAX call to prevent hanging when trying to parse an enormous page.

### 0.5.1

* Updated Parsedown to `v1.0.1`
* Added [ParsedownExtra][parsedown-extra], `v0.2.2`
* Altered Parsedown core to disable [GitHub Flavored Markdown][gfm]'s autolinking feature (it was breaking shortcode attributes)
