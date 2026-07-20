---
commendations_total: 29
commendations_mission: 0
demerits_total: 16
demerits_mission: 0
attentiveness_max: 0
attentiveness: 0
duplicity_max: 0
duplicity: 0
dynamism_max: 3
dynamism: 3
empathy_max: 0
empathy: 0
initiative_max: 3
initiative: 2
persistence_max: 1
persistence: 1
presence_max: 0
presence: 0
professionalism_max: 3
professionalism: 3
subtlety_max: 0
subtlety: 0
---
## Overall Totals

Commendations: `VIEW[{commendations_total}]`
Demerits: `VIEW[{demerits_total}]`
## Mission
```meta-bind-button
label: "Gain Demerit"
hidden: true
id: "gain-demerit"
style: default
actions:
  - type: updateMetadata
    bindTarget: demerits_mission
    evaluate: true
    value: x+1

```
```meta-bind-button
label: "Gain Commendation"
hidden: true
id: "gain-commendation"
style: default
actions:
  - type: updateMetadata
    bindTarget: commendations_mission
    evaluate: true
    value: x+1

```
```meta-bind-button
label: "Lose Commendation"
hidden: true
id: "lose-commendation"
style: default
actions:
  - type: updateMetadata
    bindTarget: commendations_mission
    evaluate: true
    value: Math.max(0, x-1)

```
```meta-bind-button
label: "Lose Demerit"
hidden: true
id: "lose-demerit"
style: default
actions:
  - type: updateMetadata
    bindTarget: demerits_mission
    evaluate: true
    value: Math.max(0, x-1)

```
```meta-bind-button
label: "End Mission"
hidden: true
id: "end-mission"
style: default
actions:
  - type: updateMetadata
    bindTarget: demerits_total
    evaluate: true
    value: getMetadata('demerits_mission')+x
  - type: updateMetadata
    bindTarget: commendations_total
    evaluate: true
    value: getMetadata('commendations_mission')+x
  - type: updateMetadata
    bindTarget: demerits_mission
    evaluate: false
    value: 0
  - type: updateMetadata
    bindTarget: commendations_mission
    evaluate: false
    value: 0

```
Commendations: `VIEW[{commendations_mission}]`
`BUTTON[lose-commendation,gain-commendation]`
Demerits: `VIEW[{demerits_mission}]`
`BUTTON[lose-demerit,gain-demerit]`

`BUTTON[end-mission]`
### Competencies
##### Attentiveness: `VIEW[{attentiveness}]`
`BUTTON[attentiveness-decrement, attentiveness-reset, attentiveness-increment]`
```meta-bind-button
label: "Reset"
hidden: true
id: "attentiveness-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: attentiveness
    evaluate: true
    value: getMetadata('attentiveness_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "attentiveness-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: attentiveness
    evaluate: true
    value: Math.min(x+1, getMetadata('attentiveness_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "attentiveness-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: attentiveness
    evaluate: true
    value: Math.max(x-1, 0)

```
##### Duplicity: `VIEW[{duplicity}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "duplicity-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: duplicity
    evaluate: true
    value: getMetadata('duplicity_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "duplicity-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: duplicity
    evaluate: true
    value: Math.min(x+1, getMetadata('duplicity_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "duplicity-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: duplicity
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[duplicity-decrement, duplicity-reset, duplicity-increment]`
##### Dynamism:`VIEW[{dynamism}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "dynamism-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: dynamism
    evaluate: true
    value: getMetadata('dynamism_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "dynamism-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: dynamism
    evaluate: true
    value: Math.min(x+1, getMetadata('dynamism_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "dynamism-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: dynamism
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[dynamism-decrement, dynamism-reset, dynamism-increment]`
##### Empathy: `VIEW[{empathy}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "empathy-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: empathy
    evaluate: true
    value: getMetadata('empathy_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "empathy-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: empathy
    evaluate: true
    value: Math.min(x+1, getMetadata('empathy_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "empathy-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: empathy
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[empathy-decrement, empathy-reset, empathy-increment]`
##### Initiative: `VIEW[{initiative}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "initiative-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: initiative
    evaluate: true
    value: getMetadata('initiative_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "initiative-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: initiative
    evaluate: true
    value: Math.min(x+1, getMetadata('initiative_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "initiative-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: initiative
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[initiative-decrement, initiative-reset, initiative-increment]`
##### Persistence: `VIEW[{persistence}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "persistence-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: persistence
    evaluate: true
    value: getMetadata('persistence_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "persistence-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: persistence
    evaluate: true
    value: Math.min(x+1, getMetadata('persistence_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "persistence-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: persistence
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[persistence-decrement, persistence-reset, persistence-increment]`
##### Presence: `VIEW[{presence}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "presence-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: presence
    evaluate: true
    value: getMetadata('presence_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "presence-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: presence
    evaluate: true
    value: Math.min(x+1, getMetadata('presence_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "presence-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: presence
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[presence-decrement, presence-reset, presence-increment]`
##### Professionalism: `VIEW[{professionalism}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "professionalism-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: professionalism
    evaluate: true
    value: getMetadata('professionalism_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "professionalism-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: professionalism
    evaluate: true
    value: Math.min(x+1, getMetadata('professionalism_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "professionalism-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: professionalism
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[professionalism-decrement, professionalism-reset, professionalism-increment]`
##### Subtlety: `VIEW[{subtlety}]`
```meta-bind-button
label: "Reset"
hidden: true
id: "subtlety-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: subtlety
    evaluate: true
    value: getMetadata('subtlety_max')

```
```meta-bind-button
label: "+1"
hidden: true
id: "subtlety-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: subtlety
    evaluate: true
    value: Math.min(x+1, getMetadata('subtlety_max'))

```
```meta-bind-button
label: "-1"
hidden: true
id: "subtlety-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: subtlety
    evaluate: true
    value: Math.max(x-1, 0)

```
`BUTTON[subtlety-decrement, subtlety-reset, subtlety-increment]`

[[Barista]]
### Sanctioned Behaviors
Receive 1 Commendation each time you:
- [x] Make someone feel welcome.
- [x] Show off your specialized knowledge.
- [x] Get some blood flowing.

## Reality: 
[[Caretaker]]
#### Relationships:
[[Chris Walsh]]
[[Ralph Avery]]
[[Jeffy Jameson]]
[[Dependent-Gregor]]
## Anomaly: 
[[Eyes]]
[[Overclock]]
[[Endbringer]]
[[Limbs]]
[[Refined Senses]]
[[I'll Cover You!]]
#### Escaped Anomalies
[[Maxentius]]
[[Voyagers of Heroia]]
