# parse subjson

package to loop json with subjson list ``pip install parse-subjson==0.1``

## how to use

1. import function of the package ``from parse_subjson import call_parser```

2. send data in format json
    ```
    data = {
        "glossary": {
            "title": "example glossary",
            "GlossDiv": {
                "title": "S",
                "GlossList": {
                    "GlossEntry": {
                        "ID": "SGML",
                        "SortAs": "SGML",
                        "GlossTerm": "Standard Generalized Markup Language",
                        "Acronym": "SGML",
                        "Abbrev": "ISO 8879:1986",
                        "GlossDef": {
                            "para": "A meta-markup language, used to create markup languages such as DocBook.",
                            "GlossSeeAlso": ["GML", "XML"]
                        },
                        "GlossSee": "markup"
                    }
                }
            }
        }
    }
    ```

3. send the parameters in the function
    ```
    r = call_parser(data)

    print(r)
    ```

4. finish and result
    ```
    {'title': 'S', 'ID': 'SGML', 'SortAs': 'SGML', 'GlossTerm': 'Standard Generalized Markup Language', 'Acronym': 'SGML', 'Abbrev': 'ISO 8879:1986', 'para': 'A meta-markup language, used to create markup languages such as DocBook.', 'GlossSee': 'markup'}
    ```