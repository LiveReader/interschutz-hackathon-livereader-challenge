# Operator Templates

Take a look at the Templates and which payload properties are required for each Template.

## Operation

```json
{
	"id": "node",
	"shape": {
		"type": "operation",
		"scale": 1
	},
	"payload": {
		"status": "red", // red, yellow, green
		"label": "VU Schwer",
		"location": "Kaiserwörthdamm 1\n67065 Ludwigshafen am Rhein",
		"affected_persons": "2",
		"affected_objects": "3",
		"tags": ["Autobahn", "Brücke"]
	}
}
```

<p align="center">
	<img src="/assets/operation.svg" style="width:30%"/>
</p>

## Emergency Reporter

```json
{
	"id": "node",
	"shape": {
		"type": "emergency-reporter",
		"scale": 1
	},
	"payload": {
		"name": {
			"first": "Maximilian",
			"last": "Mustermann"
		},
		"pending": false, // searching indicator
		"location": "Kaiserwörthdamm 1\n67065 Ludwigshafen am Rhein",
		"category": "automatic-system",
		"label": "police-department",
		"callback_number": "123"
	}
}
```

The `category` parameter has multiple options and will be represented in the tag color.

| Category          | Color                                                                                                    |
| ----------------- | -------------------------------------------------------------------------------------------------------- |
| ambulance         | <span style="padding: 5px; border-radius: 10px; background-color: #4db6ac; color:#ffffff">#4db6ac</span> |
| police-department | <span style="padding: 5px; border-radius: 10px; background-color: #81c784; color:#ffffff">#81c784</span> |
| fire-department   | <span style="padding: 5px; border-radius: 10px; background-color: #e57373; color:#ffffff">#e57373</span> |
| control-center    | <span style="padding: 5px; border-radius: 10px; background-color: #ffb74d; color:#ffffff">#ffb74d</span> |
| automatic-system  | <span style="padding: 5px; border-radius: 10px; background-color: #9575cd; color:#ffffff">#9575cd</span> |
| civilian          | <span style="padding: 5px; border-radius: 10px; background-color: #4fc3f7; color:#ffffff">#4fc3f7</span> |

<p align="center">
	<img src="/assets/emergency-reporter.svg" style="width:30%"/>
</p>

## Affected Person

```json
{
	"id": "node",
	"shape": {
		"type": "affected-person",
		"scale": 1
	},
	"payload": {
		"status": "red", // red, yellow, green
		"name": {
			"first": "Maximilian",
			"last": "Mustermann"
		},
		"sex": "Männlich",
		"age": "42",
		"accessibility": "Exponierte Lage",
		"tags": ["bewusstlos", "Verletzung: Kopf", "Puls: schwach", "Diabetes", "atmend"]
	}
}
```

<p align="center">
	<img src="/assets/affected-person.svg" style="width:30%"/>
</p>

## Affected Object

```json
{
	"id": "node",
	"shape": {
		"type": "affected-object",
		"scale": 1
	},
	"payload": {
		"status": "red", // red, yellow, green
		"label": "Rathaus Ludwigshafen",
		"accessibility": "Versperrtes Gelände",
		"tags": ["Öffentliches Gebäude"]
	}
}
```

<p align="center">
	<img src="/assets/affected-object.svg" style="width:30%"/>
</p>

## Emergency Action

```json
{
	"id": "node",
	"shape": {
		"type": "emergency-action",
		"scale": 1
	},
	"payload": {
		"category": "ambulance",
		"status": "scheduled", // scheduled, in-progress, completed
		"label": "Transport",
		"priority": "mit O2",
		"tags": ["liegend", "Sonderrechte Ziel", "Winterberg KH", "Monitor", "mit Bearmung"]
	}
}
```

The `category` parameter has multiple options and will be represented in the banner color.

| Category         | Color                                                                                                    |
| ---------------- | -------------------------------------------------------------------------------------------------------- |
| ambulance        | <span style="padding: 5px; border-radius: 10px; background-color: #4db6ac; color:#ffffff">#4db6ac</span> |
| emergency-rescue | <span style="padding: 5px; border-radius: 10px; background-color: #9575cd; color:#ffffff">#9575cd</span> |
| fire-department  | <span style="padding: 5px; border-radius: 10px; background-color: #e57373; color:#ffffff">#e57373</span> |

The `status` parameter has multiple options as well. It will be represented as a status icon

| Status      |                       Icon                       |
| ----------- | :----------------------------------------------: |
| scheduled   |  <img src="/assets/scheduled.svg" height="32"/>  |
| in-progress | <img src="/assets/in-progress.svg" height="32"/> |
| completed   |  <img src="/assets/completed.svg" height="32"/>  |

<p align="center">
	<img src="/assets/emergency-action.svg" style="width:30%"/>
</p>

## Emergency Ressource

```json
{
	"id": "node",
	"shape": {
		"type": "emergency-ressource",
		"scale": 1
	},
	"payload": {
		"status": "1", // 0 - 8
		"label": "11/83-02",
		"time_label": "bräuchte ca. 9 Minuten",
		"alerted": true
	}
}
```

<p align="center">
	<img src="/assets/emergency-ressource.svg" style="width:30%"/>
</p>

The `emergency-ressource` knows predefined `status` values and will be represented in the status color. This table shows them all and their meaning.

<p align="center">
	<img src="/assets/emergency-ressource-table.svg" style="width:60%"/>
</p>
