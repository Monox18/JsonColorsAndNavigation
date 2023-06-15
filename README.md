# JsonSymbolsAndColorSyntax JSCS
JSCS: add symbols and colorful syntax to JSON files in Sublime Text (ST)

## Coloring Syntax support
JSCS supports syntax coloring for the default themes `Mariana` and `Monokai` with multiple levels of nesting. Keys are colored according to nested level, while values are left to the default theme colors. 

Rather than creating a new syntax color, JSCS makes use of [Sublime Text configuration system](https://www.sublimetext.com/docs/settings.html). The syntax coloring is done in `<theme-name>.sublime-color-scheme`. You can select the theme via `Preferences > Select Color Scheme...`. You can add changes in you User folder to extend both the Default and JSCS configurations of the current Color Scheme via `Preferences > Customize Color Scheme`. More information in [ST Color Scheme](https://www.sublimetext.com/docs/color_schemes.html)

The inheritance is as follow:
1) `Packages/Color Scheme - Default/Mariana.sublime-color-scheme` (Default ST)
2) `Packages/JSON Symbols and Color Syntax/Mariana.sublime-color-scheme` (this repository)
3) `Packages/User/Mariana.sublime-color-scheme` (your configuration)

## Scopes
JSCS doesn't add new scopes neither extends the default scopes found in the YAML file `Packages/JSON/JSON.sublime-syntax`. That is entirely done and maintained by ST. Only the default scopes defined there are used by JSCS. This ensures that 1) JSCS works with the default .json Syntax (without creating a new one), 2) JSCS will remain compatible with future updates.

If interested into extending it, you can use [PackageResourceViewer](https://github.com/skuroda/PackageResourceViewer) to explore its contents and play around with it.

## Symbols
ST doesn't push JSON symbols `Goto > Go to Symbol` or `ctrl+R`. So JSCS pushes keys as symbols to enable code navigation. Also other plugins that make use of symbols will be ale to render and interact them. 

## Json outline (aka Table of Contents)
I recommend you the [Outline package](https://github.com/warmdev/SublimeOutline) which enables a code navigation, function navigation, symbol navigation, whatever you want to call it. A clicable list of idented keys will be show and you can interact with them
