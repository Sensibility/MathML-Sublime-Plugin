# MathML-Sublime-Plugin
A Package for MathML syntax highlighting and basic snippets in Sublime Text 3.x
This package enforces a subset of the W3C MathML 3.0 standard, which can be found [here](https://www.w3.org/TR/MathML3/).
Unlike HTML, MathML does NOT meaningfully allow arbitrary attributes on any and all tags, so don't expect it to highlight them. The package does currently support all presentation elements listed on MDN [here](https://developer.mozilla.org/en-US/docs/Web/MathML/Element). A large subset of attributes is also supported. However, by default, highlighting is only available in dedicated mathml files with the extensions:
* `.mathml`
* `.mathm`
* `.math`

which is to say, not inside of HTML (that functionality is planned, however).
I highly recommend checking out the MDN documentation for examples and reference materials when writing MathML.
