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

