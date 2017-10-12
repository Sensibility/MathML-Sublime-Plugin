# MathML-Sublime-Plugin
## About
A Package for MathML syntax highlighting and basic snippets in Sublime Text 3.x
This package enforces a subset of the W3C MathML 3.0 standard, which can be found [here](https://www.w3.org/TR/MathML3/).
Unlike HTML, MathML does NOT meaningfully allow arbitrary attributes on any and all tags, so don't expect it to highlight them. The package does currently support all presentation elements listed on MDN [here](https://developer.mozilla.org/en-US/docs/Web/MathML/Element). Nearly all valid attributes are also supported, albeit with exclusion of some deprecated MathML 2.0 features, and no support for xml namespace-included attributes. By default, highlighting is available in dedicated mathml files as well as inside special html files with the extensions:
* `.mathml` (also `.html.mathml`, somewhat reduntantly)
* `.mathm`
* `.math` (also `.html.math`, somewhat reduntantly)
* `.mhtml`

If you want highlighting for MathML inside of files without these extensions, use the command palette or select it from the menu under View -> Syntax -> MathML -> HTML (MathML)

I highly recommend checking out the MDN documentation for examples and reference materials when writing MathML - especially since Firefox is the only browser that natively supports MathML. A Chrome Extension which enables rendering of MathML within web pages is available [here](https://chrome.google.com/webstore/detail/fmath-html-%2B-mathml-solut/emdjdpchbjipnjhkfljbcapgfecmnglm).

## Installation
### Manual
>To install, clone or download this repository into your Packages directory (`%APPDAT%\SUBLIME TEXT 3\PACKAGES` on Windows or `$HOME/.config/sublime-text-3/Packages` on Linux/macOS). For Linux/macOS users with `git` installed, enter these commands at a terminal:

* `cd $HOME/.config/sublime-text-3/Packages` - enter Packages directory
* `git clone git@github.com:Sensibility/MathML-Sublime-Plugin` - download the plugin
* `mv MathML-Sublime-Plugin MathML` - rename package to something simpler (optional)

>Then, if you want, remove any unnecessary files like e.g. `.gitignore`. Or don't. Should work either way.

### Pre-packaged
>As of version 1.2.0, full packages are available as compressed `.sublime-package` files under "Releases" ([here](https://github.com/Sensibility/MathML-Sublime-Plugin/releases)).

## Planned Features

Currently still in the works are the following features:

* Integration with Package Control - Pull request pending
* Completions for supported elements
* More snippets (or possibly less if completions prove easier and faster)
* Enforced values for attributes, including
	* Highlighting invalid values as illegal
	* Highlighting missing units on values that require them as illegal
	* Highlighting deprecated values as deprecated
* A linting system to check files to ensure that e.g. all `<mfrac>` tags have exactly two children, with a supporting build system
* Content-MathML - This is essentially another markup language specified by MathML 3.0, meant to convey the meaning of mathematical formulae without providing a way to represent it (which is what Presentation-MathML is for).
* Annotations - Annotations provide extra information about math markup, and are often used to define alternative representations such as LaTeX code. I'd like to support some additional syntaxes if they exist, but I need to know more about the Sublime Package system first and so this is a relatively low priority.
