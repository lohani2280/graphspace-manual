# GraphSpace Network Model

## CYJS Format

GraphSpace only supports one of the [Cytoscape.js supported](http://js.cytoscape.org/#getting-started/specifying-basic-options) JSON formats, which is:

```
{
    elements:{
        nodes:[
            {
                data: { 
                    id: ...
                },
                position: { 
                    x: ...
                    y: ...
                }
            }, 
            .
            .
        ],
        edges:[
            {
                data: { 
                    source: ...,
                    target: ...
                }
            }, 
            .
            .
        ]
    }
}
```

This [JSON (JavaScript Object Notation)](http://www.json.org/) format is defined by Cytoscape for storing network structure and data information. A Cytoscape (v3.1 or later) user can easily [export their graph](http://manual.cytoscape.org/en/stable/Cytoscape.js_and_Cytoscape.html#export-network-and-table-to-cytoscape-js) in above mentioned JSON format. We call the format as `CYJS format` because the extension of the exportable JSON file from Cytoscape App is `.cyjs`.

## Stylesheet JSON Format

Cytoscape and Cytoscape.js are sharing a concept called [Style](http://manual.cytoscape.org/en/stable/Cytoscape.js_and_Cytoscape.html#export-styles-to-cytoscape-js). This is a collection of mappings from data point to network property. Cytoscape can export its Styles into CSS-based Cytoscape.js JSON. 

A Cytoscape (v3.1 or later) user can export all Styles into one JSON file from **File | Export | Style** and select Cytoscape.js JSON as its format.

**Note:** Cytoscape.js [does not support all of Cytoscape Network Properties](
http://manual.cytoscape.org/en/stable/Cytoscape.js_and_Cytoscape.html#limitations). Those properties will be ignored or simplified when you export to JSON Style file.