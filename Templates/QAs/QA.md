<%* 
const qaName = await tp.system.prompt("Enter QA name");
%>


```meta-bind-button
label: "Reset"
hidden: true
id: "<% qaName %>-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: <% qaName %>
    evaluate: true
    value: getMetadata('<% qaName %>_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "<% qaName %>-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: <% qaName %>
    evaluate: true
    value: Math.min(x+1, getMetadata('<% qaName %>_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "<% qaName %>-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: <% qaName %>
    evaluate: true
    value: Math.max(x-1, 0)

```