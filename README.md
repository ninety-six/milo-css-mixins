# Milo CSS Mixins
An array of CSS Utility classes to be used in your Milo CSS-based framework.

## Installation
```npm i @milo-css/mixins```

## Functions
### Color
```@import "node_modules/@milo-css/mixins/color";```

| Usages | Description | Note |
|---|---|---|
| ```color("black")``` | Get color by name from ```colors()``` map variable | Requires ```colors()``` map variable |
| ```color-a("black", .6)``` | Get color by name from ```colors()``` map variable with an alpha value | Requires ```colors()``` map variable |
| ```color-lighten("black", 30%)``` | Lighten a color by name from ```colors()``` map variable by a percentage | Requires ```colors()``` map variable |
| ```color-darken("white", 30%)``` | Darken a color by name from ```colors()``` map variable by a percentage | Requires ```colors()``` map variable |


### Z-index
```@import "node_modules/@milo-css/mixins/z-index";```

| Usage | Description | Note |
|---|---|---|
| ```zindex("top")``` | Get z-index value by name from ```$z-layers()``` map variable | Requires ```$z-layers()``` map variable |


## Mixins
### Centerer
```@import "node_modules/@milo-css/mixins/centerer";```

| Usages | Description | Note |
|---|---|---|
| ```@include centerer(true, true);``` | Position an element centrally horizontally & vertically | Ensure parent element has ```position: relative;``` |
| ```@include centerer(true, false);``` | Position an element centrally horizontally | Ensure parent element has ```position: relative;``` |
| ```@include centerer(false, true);``` | Position an element centrally vertically | Ensure parent element has ```position: relative;``` |


### Clearfix
```@import "node_modules/@milo-css/mixins/clearfix";```

| Usage | Description |
|---|---|
| ```@include clearfix;``` | Used to clear a floating element |


### Gradient
```@import "node_modules/@milo-css/mixins/gradient";```

| Usage | Description | Note |
|---|---|---|
| ```@include gradient(color("black"), 'to bottom'));``` | Produces a smoother, more aesthetically pleasing gradient | ```color``` value can be a hexcode, rgb or provided by the ```color()``` function |


### Grid
```@import "node_modules/@milo-css/mixins/grid";```

| Usages | Description |
|---|---|
| ```@include css-grid(1fr 1fr 1fr, 1fr 1fr 1fr, 15px);``` | Basic CSS Grid maker |
| ```@include place-css-grid-items((1 3 1 1, 1 2 2 1, 1 1 2 2, 1 3 3 1));``` | Set properties and place an array of grid items |


### Image
```@import "node_modules/@milo-css/mixins/image";```

| Usage | Description |
|---|---|
| ```@include img-fluid;``` | Gives an image responsive properties |


### Margin
```@import "node_modules/@milo-css/mixins/margin";```

| Usages | Description |
|---|---|
| ```@include margin('x', 1.5rem);``` | Outputs ```margin-left: 1.5rem; margin-right: 1.5rem;``` |
| ```@include margin('r', 1.5rem);``` | Outputs ```margin-right: 1.5rem;``` |
| ```@include margin;``` | Outputs ```margin: 0;``` |


### Padding
```@import "node_modules/@milo-css/mixins/padding";```

| Usages | Description |
|---|---|
| ```@include padding('x', 1.5rem);``` | Outputs ```padding-left: 1.5rem; padding-right: 1.5rem;``` |
| ```@include padding('r', 1.5rem);``` | Outputs ```padding-right: 1.5rem;``` |
| ```@include padding;``` | Outputs ```padding: 0;``` |


### Position
```@import "node_modules/@milo-css/mixins/position";```

| Usage | Description |
|---|---|
| ```@include position(0, 0, 0, 0);``` | Output ```top: 0; right: 0; bottom: 0; left: 0; position: absolute;``` |


### Pseudo
```@import "node_modules/@milo-css/mixins/pseudo";```

| Usage | Description |
|---|---|
| ```@include pseudo;``` | Sets a base when styling ```:before``` or ```:after``` elements |


### Ratio
```@import "node_modules/@milo-css/mixins/ratio";```

| Usage | Description |
|---|---|
| ```@include ratio(16, 9, true);``` | Creates scalable element that maintains a 16:9 ratio |


### Shapes
```@import "node_modules/@milo-css/mixins/shapes";```

| Usage | Description | Note |
|---|---|---|
| _**Square**_||
| ```@include square(color("red"), 20px);``` | Creates a 20x20px square ||
| ```@include square(color("red"), 20px, true);``` | Creates a 20x20px square with rounded corners | Requires ```$global-radius``` variable |
| _**Rectangle**_||
| ```@include rectangle(color("red"), 20px, 10px);``` | Creates a 20x10px rectangle ||
| ```@include rectangle(color("red"), 20px, 10px, true);``` | Creates a 20x10px rectangle with rounded corners | Requires ```$global-radius``` variable |
| _**Circle**_||
| ```@include circle(color("red"), 20px);``` | Creates a 20px diameter circle ||
| _**Oval**_||
| ```@include oval(color("red"), 20px, 10px);``` | Creates a 20x10px oval ||
| _**Triangle**_||
| ```@include triangle(color("red"), down, 10px);``` | Creates a 10px triangle that points down ||
| ```@include triangle(color("red"), down, 10px, true);``` | Creates a 10px triangle with rounded corners that points down | Requires ```$global-radius``` variable |
