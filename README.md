# metacatalog-msx

JSON Schema defining a metacatalog proposal for 8-bit-computer tapes, cartridges, disks...

Trying to unify and categorize all MSX software.

## Examples

###### Minimal index

```json
{
	"$schema": "https://raw.githubusercontent.com/nataliapc/metacatalog-msx/master/schemas/index.schema.json",
	"header": {
		"mimecrc": "d98d4159",
		"mimetype": "application/x-metacatalog-tape",
		"version": "1.0.0"
	},
	"catalog": {
		"id": {
			"string": "msx.game.cas.mygame.1986.alternateVersion2.es.spain",
			"crc32": "7b907a15",
			"md5": "8120c7da7a1f6d5248d5a98897fd901a",
			"sha1": "7b755b329a2db85bd1b8dd8b90338e1d870368ce"
		},
		"updated": "2016-12-22 11:19:50",
		"platform": "MSX",
		"type": "game",
		"name": "MyGame",
		"license": "commercial"
	},
	"content": [
		{
			"id": "tape1.sideA",
			"mimetype": "application/x-msx-cas",
			"file": "content/tape1sideA.cas"
		}
	]
}
```

###### Simple case with just a tape and several images

```json
{
    "$schema": "https://raw.githubusercontent.com/nataliapc/metacatalog-msx/master/schemas/index.schema.json",
    "header": {
        "mimecrc": "d98d4159",
        "mimetype": "application/x-metacatalog-tape",
        "version": "1.0.0"
    },
    "catalog": {
        "id": {
            "string": "msx.game.cas.mygame.1986.alternateVersion2.es.spain",
            "crc32": "7b907a15",
            "md5": "8120c7da7a1f6d5248d5a98897fd901a",
            "sha1": "7b755b329a2db85bd1b8dd8b90338e1d870368ce"
        },
        "updated": "2016-12-22 11:19:50",
        "platform": "MSX",
        "type": "game",
        "name": "MyGame name",
        "name.original": "MyGame original name",
        "company": "MyCompany",
        "publisher": "MYPublisher",
        "license": "commercial",
        "date": 1986,
        "country": "Spain",
        "genre": [
            "action",
            "puzzle"
        ],
        "language": [
            "es",
            "en",
            "jp"
        ],
        "authors": [
            {
                "name": "MyName",
                "job": "my job"
            }
        ],
        "instructions": "plain text with the cover text"
    },
    "extras": {
        "images": [
            {
                "id": "tape.cover",
                "file": "images/cover1.jpg",
                "label": ""
            },
            {
                "id": "tape.back",
                "file": "images/back1.jpg",
                "label": ""
            },
            {
                "id": "tape.sideA",
                "file": "images/tape1SideA.jpg",
                "label": ""
            },
            {
                "id": "tape.cover#restored",
                "default": true,
                "file": "images/cover.restored.jpg",
                "label": ""
            },
            {
                "id": "manual.page1",
                "file": "images/manual_1.png",
                "label": "Manual page 1",
                "label.es": "Manual página 1"
            },
            {
                "id": "manual.page2",
                "file": "images/manual_2.png",
                "label": "Manual page 2",
                "label.es": "Manual página 2"
            },
            {
                "id": "screenshot.1",
                "file": "images/screenshot_1.png",
                "label": "Game screenshot",
                "label.es": "Pantallazo del juego"
            },
            {
                "id": "game.map",
                "file": "images/map.png",
                "label": "Game map",
                "label.es": "Mapa del juego"
            }
        ]
    },
    "content": [
        {
            "id": "tape1.sideA",
            "label": "Tape 1 Side A",
            "mimetype": "application/x-msx-cas",
            "file": "content/tape1sideA.cas",
            "comment": "Tape file",
            "related.images": [
                "tape.cover",
                "tape.back",
                "tape.sideA"
            ]
        }
    ]
}
```
