---
name: c4
display_name: C4 (C4-PlantUML)
description: The C4 library enables a simple way of describing and communicate software architectures with an intuitive language.
author: kirchsth, Victor Lupu and Ricardo Niepel
version: 2.11.0
release: https://github.com/plantuml-stdlib/C4-PlantUML/tree/release/v2.11.0

source: https://github.com/plantuml-stdlib/C4-PlantUML
issues: https://github.com/plantuml-stdlib/C4-PlantUML/issues
discussions: https://github.com/plantuml-stdlib/C4-PlantUML/discussions
license: MIT
license_details: https://github.com/plantuml-stdlib/C4-PlantUML/blob/master/LICENSE
copyright: Copyright (c) 2020 - 2025 kirchsth, Victor Lupu and Ricardo Niepel
---

## C4 library (C4-PlantUML) [C4]

|property      | value                    |
|--------------|--------------------------|
|name:         | c4                       |
|display_name: | C4 (C4-PlantUML)         |
|description:  | The C4 library enables a simple way of describing and communicate software architectures with an intuitive language.
|author:       | kirchsth, Victor Lupu and Ricardo Niepel
|version:      | 2.11.0                   |
|release:      | https://github.com/plantuml-stdlib/C4-PlantUML/tree/release/v2.11.0
|              |                          | 
|source:       | https://github.com/plantuml-stdlib/C4-PlantUML
|issues:       | https://github.com/plantuml-stdlib/C4-PlantUML/issues
|discussions:  | https://github.com/plantuml-stdlib/C4-PlantUML/discussions
|license:      | MIT, details see [LICENSE](https://github.com/plantuml-stdlib/C4-PlantUML/blob/master/LICENSE)
|copyright:    | Copyright (c) 2020 - 2025 kirchsth, Victor Lupu and Ricardo Niepel

===========================

![name: C4](https://img.shields.io/badge/name-C4-blue)
![display_name: C4 (C4-PlantUML)](https://img.shields.io/badge/display__name-C4_(C4--PlantUML)-blue)
![version: 2.11.0](https://img.shields.io/badge/version-2.11.0-blue)
![release: https://github.com/plantuml-stdlib/C4-PlantUML/tree/release/v2.11.0](https://img.shields.io/badge/release-https://github.com/plantuml--stdlib/C4--PlantUML/tree/release/v2.11.0-orange)
<br>
![author: kirchsth, Victor Lupu and Ricardo Niepel](https://img.shields.io/badge/author-kirchsth,_Victor_Lupu_and_Ricardo_Niepel-blue)
<br>
![description: The C4 library enables a simple way of describing and communicate software architectures with an intuitive language.](https://img.shields.io/badge/description-The_C4_library_enables_a_simple_way_of_describing_and_communicate_software_architectures_with_an_intuitive_language.-blue)

![source: C4](https://img.shields.io/badge/source-https://github.com/plantuml--stdlib/C4--PlantUML-orange)
<br>
![issues: C4](https://img.shields.io/badge/issues-https://github.com/plantuml--stdlib/C4--PlantUML/issues-orange)
<br>
![discussions: C4](https://img.shields.io/badge/discussions-https://github.com/plantuml--stdlib/C4--PlantUML/discussions-orange)
<br>
![license: C4](https://img.shields.io/badge/license-MIT-green)
![license_details: C4](https://img.shields.io/badge/license__details-https://github.com/plantuml--stdlib/C4--PlantUML/blob/master/LICENSE-orange)
<br>
![copyright: C4](https://img.shields.io/badge/copyright-Copyright_(c)_2020_--_2025_kirchsth,_Victor_Lupu_and_Ricardo_Niepel-orange)

===========================

![name: C4](https://img.shields.io/badge/name-C4-blue)
![display_name: C4 (C4-PlantUML)](https://img.shields.io/badge/display__name-C4_(C4--PlantUML)-blue)
![version: 2.11.0](https://img.shields.io/badge/version-2.11.0-blue)
![license: C4](https://img.shields.io/badge/license-MIT-green)
<br>
![author: kirchsth, Victor Lupu and Ricardo Niepel](https://img.shields.io/badge/author-kirchsth,_Victor_Lupu_and_Ricardo_Niepel-blue)
<br>
![description: The C4 library enables a simple way of describing and communicate software architectures with an intuitive language.](https://img.shields.io/badge/description-The_C4_library_enables_a_simple_way_of_describing_and_communicate_software_architectures_with_an_intuitive_language.-blue)

![all properties see: /C4/README.md](https://img.shields.io/badge/all_properties_see-./stdlib/C4/README.md-orange)

The C4 library enables a simple way of describing and communicate software architectures with an intuitive language.

It is the PlantUML integrated version of [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML) and has the big advantage that it can be used without additional external includes.
(E.g. container diagrams can be drawn with `!include <C4/C4_Container>` and no `!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml` is required.)

Example of usage:

```plantuml
@startuml
!include <C4/C4_Container>
LAYOUT_LEFT_RIGHT()

Person(admin, "Administrator")
System_Boundary(c1, "Sample System") {
    Container(web_app, "Web Application", "C#, ASP.NET Core 2.1 MVC", "Allows users to compare multiple Twitter timelines")
}
System(twitter, "Twitter")

Rel(admin, web_app, "Uses", "HTTPS")
Rel(web_app, twitter, "Gets tweets from", "HTTPS")

SHOW_LEGEND()
@enduml
```

This example renders the following image:

[![Example](https://www.plantuml.com/plantuml/png/JL1TQy9047o_Nx5DNn8GYyN7KanJgmMhOivAdyAPRE7WFiBT1f7I_zvDjTfxMUvcPcTk9f5KeCuQSQDTRRe6uQ4OtnNZgl2Eb7OO7iKY_rXjPRMOliXgypgRopGJOeqXUfUgncetW2JlfuuK5FcGPA8yHa9RFVdEDIeSqth4f5BPrY2Si2I3Bm5yBaxf0VULQbjcxd0FUTiQNIlItYNyLDmE82_Nm-LKiYGWt0z7yFPUz5XkZ3z4w2A62EIXzhPLJB6T8TrRoeCcmW2aBHhsYXpn-nmofHF8Uyuq1iK6pT_dhh6saPKyvrAkooJx9LtGwvePKkGhzkCpUFjV8ihvQiTTpgRBP-vnWgxX-dy0)](https://www.plantuml.com/plantuml/uml/JL1TQy9047o_Nx5DNn8GYyN7KanJgmMhOivAdyAPRE7WFiBT1f7I_zvDjTfxMUvcPcTk9f5KeCuQSQDTRRe6uQ4OtnNZgl2Eb7OO7iKY_rXjPRMOliXgypgRopGJOeqXUfUgncetW2JlfuuK5FcGPA8yHa9RFVdEDIeSqth4f5BPrY2Si2I3Bm5yBaxf0VULQbjcxd0FUTiQNIlItYNyLDmE82_Nm-LKiYGWt0z7yFPUz5XkZ3z4w2A62EIXzhPLJB6T8TrRoeCcmW2aBHhsYXpn-nmofHF8Uyuq1iK6pT_dhh6saPKyvrAkooJx9LtGwvePKkGhzkCpUFjV8ihvQiTTpgRBP-vnWgxX-dy0)
