## Active Color Coding for Solidity Override
This code will activate solidity override color coding in your syntax highlighting for the "Solidity Language & Themes (only)" extension.

Change the following line to activate additional color coding for solidity override.

```json
src/syntaxes/solidity.tmLanguage.json


"declaration-visibility": {
    "patterns": [
        {
            "match": "\\b(private|internal|constant|immutable|pure|view|nonpayable|indexed)\\b",
            "name": "storage.type.modifier.keyword.solidity"
        },
        {
            "match": "\\b(public|external|payable|inherited|storage|memory|calldata|override)\\b",
            "name": "storage.type.modifier.keyword.extendedscope.solidity"
        }
    ]
},
```

"override" is added in the "match" section.

### Additional Color Coding
If you want to give additional color to the funcition name that is overridden, you can add the following code:

```json
src/themes/dark_sva_default_highlights.json


{
    "name":"function override",
    "scope":"entity.name.function.override.solidity",
    "settings": {
        "foreground": "#61AFEF",
        "fontStyle": "bold underline"
    }
},
```

and replace the "declaration-function" section like below:

```json
src/syntaxes/solidity.tmLanguage.json


"declaration-function": {
    "patterns": [
        {
            "include": "#declaration-function-override"
        },
        {
            "include": "#declaration-function-regular"
        }
    ]
},
"declaration-function-override": {
    "begin": "\\b(function)\\s+([A-Za-z_]\\w*)\\b(?=.*\\boverride\\b)",
    "beginCaptures": {
        "1": {
            "name": "storage.type.function.solidity"
        },
        "2": {
            "name": "entity.name.function.override.solidity"
        }
    },
    "end": "({)",
    "endCaptures": {
        "1": {
            "name": "punctuation.block.solidity"
        }
    },
    "patterns": [
        {
            "include": "#method-head"
        }
    ]
},
"declaration-function-regular": {
    "begin": "\\b(function)\\s+([A-Za-z_]\\w*)\\b",
    "beginCaptures": {
        "1": {
            "name": "storage.type.function.solidity"
        },
        "2": {
            "name": "entity.name.function.solidity"
        }
    },
    "end": "({)",
    "endCaptures": {
        "1": {
            "name": "punctuation.block.solidity"
        }
    },
    "patterns": [
        {
            "include": "#method-head"
        }
    ]
},
```



