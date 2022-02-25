# Lab Report 4 Week 8
`Valid Links and JUnit`
### By: Andrew Pan

## Markdown-Parse Repositories
- [Our Group](https://github.com/pandrew99/markdown-parse)
- [Reviewed Group](https://github.com/PierreBeur/markdown-parse)

## What each markdown snippet should produce 
### Snippet 1
Markdown:
```
`[a link`](url.com)
[another link](`google.com)`
[`cod[e`](google.com)
[`code]`](ucsd.edu)
```
Result: 
`[%60google.com, google.com, ucsd.edu]`

### Snippet 2
Markdown:
```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
Result:
`[a.com, a.com(()), example.com]`

### Snippet 3
Markdown:
```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```
Result:
`[https://ucsd-cse15l-w22.github.io/]`

