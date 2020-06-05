# ./jqview

The simplest possible native GUI for inspecting JSON objects with [jq](https://stedolan.github.io/jq/manual/).

Made with [fyne](https://fyne.io/) and [gojq](https://github.com/itchyny/gojq).

## Usage

```
~> echo '[{"name": "Mises"}, {"name": "Hayek"}, {"name": "Menger"}]' | jqview
```

![](screenshot1.png)

```
~> echo '[{"name": "Mises"}, {"name": "Hayek"}, {"name": "Menger"}]' | jqview '.[].name
```

![](screenshot2.png)

```
~> echo '[{"name": "Mises"}, {"name": "Hayek"}, {"name": "Menger"}]' > names.json
~> jqview 'map(select(.name | startswith("M")))' names.json
```

![](screenshot3.png)

## Installation

Download from [releases](https://github.com/fiatjaf/jqview/releases), or compile with

```
go get github.com/fiatjaf/jqview
```