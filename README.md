## &lt;actindo-tree&gt;  and &lt;actindo-tree-edit&gt;

`<actindo-tree>` and `<actindo-tree-edit>` for showing and modifying tree data

## Examples

### Actindo Tree

#### use remote data

when setting the *remote*, the tree will load data from the remote

```
    <actindo-tree
        remote="/your-endpoint"
        auto-load="true"
        selected="{{treeNodeSelected}}"
    >

```


#### use local data

if there isn't any setting for *remote*, the data will be loaded through *items* property

```
<actindo-tree
    items="[[items]]"
    auto-load="true"
    selected="{{treeNodeSelected}}"
>
```

```
// local data
tree: {
    type: Array,
    value: [
        {
            "id": 1,
            "name": "food",
            "children": [
             {
               "id": 31,
               "name": "street food",
               "children": [],
             }
            ]
            },
            {
            "id": 21,
            "name": "restaurant",
            "children": [
             {
               "id": 61,
               "name": "e51",
               "children": []
             }
            ]
        }
    ]
},
```

### Actindo Tree Edit

```
    <actindo-tree-edit
        data="[[tree]]"
        id="editTree"
        max-depth="2"
        remote-submit="/your-endpoint"
        on-submit="onSubmit"
        on-cancel="onCancel"
    >
    </actindo-tree-edit>

```