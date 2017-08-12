JSON to HTML Table
==================

This is a fork of the JSON To HTML table project of Afshin Mehrabani (https://github.com/afshinm/Json-to-HTML-Table).

## How to use
There's only one function in this library and accept four parameter that only the first one is required.
    
```javascript
    function ConvertJsonToTable(parsedJson, tableId, tableClassName, linkText, imgHeaders, headerNames)
```
    
Simply call `ConvertJsonToTable` method and fill the `parsedJson` parameter.  

## Example

This is an example of using this library:  

```javascript
    //Example data, Object 
    var objectArray = [{
        "tot": "34",
        "ver": "1.0.4",
        "off": "New York",
        "pic": "https://en.wikipedia.org/wiki/New_York_City#/media/File:NYC_Montage_2014_4_-_Jleon.jpg"
    }, {
        "tot": "67",
        "ver": "1.1.0",
        "off": "Paris",
        "pic": "https://en.wikipedia.org/wiki/Paris#/media/File:Seine_and_Eiffel_Tower_from_Tour_Saint_Jacques_2013-08.JPG"
    }];
    
    //Example data, Array
    var stringArray = ["New York", "Berlin", "Paris", "Marrakech", "Moscow"];
    
    //Example data for image headers, Array
    var imageColumns = ["pic"];
    
    //Example data for column names, Object
    var columnNames = {tot: "Total", ver: "Version", off: "Office", pic: "Photo"];
    
    //Example data, nested Object. This data will create nested table also.
    var nestedTable = [{
        key1: "val1",
        key2: "val2",
        key3: {
            tableId: "tblIdNested1",
            tableClassName: "clsNested",
            linkText: "Download",
            data: [{
                subkey1: "subval1",
                subkey2: "subval2",
                subkey3: "subval3"
            }]
        }
    }];
```

Code sample to create a HTML table from JSON:

```javascript
    //Only first parameter is required
    var jsonHtmlTable = ConvertJsonToTable(objectArray, 'jsonTable', null, 'Download', imageColumns, columnNames);
```

Code sample explaned:
 - First parameter is JSON data
 - table HTML id attribute will be **jsonTable**
 - table HTML class attribute will not be added
 - **Download** text will be displayed instead of the link itself
 - imageColumns array defines which headers contain image URLs
 - columnNames array defines what names should show in the HTML header

## Contributors
[Afshin Mehrabani](https://github.com/afshinm) (@afshinmeh)  
[Sgissinger](https://github.com/sgissinger) 

## Contributing

This is a open-source project. Fork the project, complete the code and send pull request.

## License

    Copyright (C) 2012 Afshin Mehrabani (afshin.meh@gmail.com)
    
    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated 
    documentation files (the "Software"), to deal in the Software without restriction, including without limitation 
    the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, 
    and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
    The above copyright notice and this permission notice shall be included in all copies or substantial portions 
    of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED 
    TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL 
    THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF 
    CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS 
    IN THE SOFTWARE.

