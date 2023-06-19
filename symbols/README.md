# About symbolTransformation

* The Regex engine is [Onigurama](https://raw.githubusercontent.com/kkos/oniguruma/master/doc/RE)
* As the regex expressions are contained within HTML tags (.tmPreferences files are HTML), then escape HTML characters. 
  * Eg. an Onigurama positive look behind group `(?<=subexp)` becomes `(?&lt;=subexp)`
* The format is `s/regexp/replacement/flags`. Aka S-command or Regex substitution.
* Each expression is terminated by `;` and can be commented with `#`. 

## Examples
* `s/(?&lt;=^.{20}).*/…/;` Replace everything after n characters `{n}` with elipsis `…`.
* `s// /;` pre-pend whitespaces (for identation effect).

### Code block example with list of Regex and comments
```html
<key>symbolTransformation</key>
<string>
  s/(?&lt;=^.{20}).*/…/; #Replace everything after n charactes {n} with elipsis ….
  s//   /; #pre-pend whitespaces (for identation effect).
</string>
```
