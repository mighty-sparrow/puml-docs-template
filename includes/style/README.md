# Style

These files are used to ensure a consistent style across diagrams. Include them in a diagram with the following lines:

If you are using the `plantuml.includepaths` in VS Code (or the `-Dplantuml.include.path` parameter from the command-line), you only need to include the file name itself. PlantUML will look for the files at those directory destinations first.
```
@startuml

!pragma teoz true

!include skinparams.iuml
!include stylesheet.iuml

@enduml

```

---
<details>
<summary>Explicit Paths</summary>

If you are not using the globally included paths, you can also explicity include a file by a full or relative path.

<sub>(...but it's not as easy to maintain).</sub>
```
@startuml

!pragma teoz true

!include ../style/skinparams.iuml
!include /Users/someuser/ProjectSource/my_puml_project/style/stylesheet.iuml

@enduml

```

</details>


---
<br/>
<br/>

# Style Pages

The following pages are used to style the diagrams, should you include them.

### `presets.iuml`

This file contains styles that can be used to customize the look and feel of your PlantUML diagrams. Within your main PlantUML file, you can define which style to use by setting the `STYLE_THEME` variable to one of the following options: `[ DEFAULT | LIGHT | DARK | MIDNIGHT | NATURAL | NATURAL_DARK | NATURAL_DARK_ALT ]`.

### `skinparams.iuml`

This file contains the skinparam definition for the PlantUML diagrams. It is included in the other PlantUML files using the !include directive and sets the default style rendering parameters for the diagrams.

Within this file you can [re]define things like the `dpi` (i.e. _resolution_) of the image.

### `stylesheet.iuml`

This file is a part of the PlantUML Styling Project. The contents of this define the default color values to use for the various PlantUML elements. The variables are defined in the `presets.iuml` file. The subset of colors used depends on the `STYLE_THEME` selected. The default theme is `DEFAULT`.