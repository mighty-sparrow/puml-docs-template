# Style

These files are used to ensure a consistent style across diagrams. Include them in a diagram with the following lines:
```java
@startuml

!pragma teoz true

!include ../style/skinparams.iuml
!include ../style/stylesheet.iuml

@enduml

```

# Style Pages

The following pages are used to style the diagrams, should you include them.

### `presets.iuml`

This file contains styles that can be used to customize the look and feel of your PlantUML diagrams. Within your main PlantUML file, you can define which style to use by setting the `STYLE_THEME` variable to one of the following options: `[ DEFAULT | LIGHT | DARK | MIDNIGHT | NATURAL | NATURAL_DARK | NATURAL_DARK_ALT ]`.

### `skinparams.iuml`

This file contains the skinparam definition for the PlantUML diagrams. It is included in the other PlantUML files using the !include directive and sets the default style rendering parameters for the diagrams.

Within this file you can [re]define things like the `dpi` (i.e. _resolution_) of the image.

### `stylesheet.iuml`

This file is a part of the PlantUML Styling Project. The contents of this define the default color values to use for the various PlantUML elements. The variables are defined in the `presets.iuml` file. The subset of colors used depends on the `STYLE_THEME` selected. The default theme is `DEFAULT`.