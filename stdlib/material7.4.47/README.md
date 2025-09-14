---
name: material7.4.47
display_name: Material
description: SVG Material Design Icon
author: Austin Andrews
version: 7.4.47
release: 
license: Apache License, Version 2.0
source: https://github.com/Templarian/MaterialDesign-SVG/
origin: 
---

**Attention: Files in this branch use partly "extended" paths that changes can be tested before they are merged into stdlib.**

# Information about the `material7.4.47` Standard Library.

## Sprites without additional dependencies

The sprites are imported from https://pictogrammers.com/library/mdi/ and organized in folders based on the given category names.

The sprites can be included via the (normalized) collection name and the (normalized) icon name. In both cases is the normalization an upper camel case notation without any special characters.

**Example:** the original icon `account-alert` belongs to the category ´Account/User´ therefore the corresponding sprite can be included via `!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/AccountUser/AccountAlert.puml` (only this icon/sprite) or `!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/AccountUser/all` (with all other icons/sprites of the collection).  
The icon `account-alert` has the category ´Alert/Error´ too, therefore it could be loaded via `!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/AccountUser/AlertError.puml` too.

The sprites itself has the (normalized) icon name with the prefix `mdi`.

**Example:** the original icon `account-alert` can be integrated in a PlantUML diagram with `<$mdiAccountAlert>`.

```plantuml
@startuml

' no common.puml loaded, text alignment remains left

!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/AccountUser/AccountAlert.puml
!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/Emoji/all.puml

package "Possible image samples\nwithout additional dependencies" {
  label "explicit loaded sprite in text\n<$mdiAccountAlert>" as accountAlertSprite

  label "sprite loaded via collection Emoji/all.puml in text\n<$mdiEmoticonLol>" as emoticonLol
}

@enduml
```
(The source of the sample can be found in [stdlib/material7.4.47/\_examples\_/OnlySpriteSample.puml](https://github.com/plantuml/plantuml-stdlib/tree/master/stdlib/material7.4.47/_examples_/OnlySpriteSample.puml))
[![PleaseOpenLinkIfImageCannotBeDisplayed](https://www.plantuml.com/plantuml/svg/lP6npXCn3CVtF8Kv8R70PQbK2I7K3cmCI8YjYoznUwQE4oK-MWdnxjorXrg-1_Ysn9P_lt_YNJEiDYLnxXreXf1JojgNkGAICL9y3qPN0nG-QI8rg9IGjO7GqPnxmnfaYWIZMMaVlQzuwKziupHCZMh8QgJMprn_vXh6PgClWheuFpIBmeElT6n-98pDpohIsUhNLaAZoYZRVjDljduVGfxKVipaV-UzKBLRu5VEyYNbd-nHv2vt1SCPJmJTjzmQ3qB0QRatJ4Me7VJ2DkR906Dauwme4Aai2WrChOFV3a1m886EhaKuiArBW5Og6m7hRHi7_VGsHNx-WSyTO0Dygdo_ZRW7SsMin5-C4B88XIKB_F-Q5wAvQHooVirozz2ZuFuujoEDyzHV)](https://www.plantuml.com/plantuml/uml/lP6npXCn3CVtF8Kv8R70PQbK2I7K3cmCI8YjYoznUwQE4oK-MWdnxjorXrg-1_Ysn9P_lt_YNJEiDYLnxXreXf1JojgNkGAICL9y3qPN0nG-QI8rg9IGjO7GqPnxmnfaYWIZMMaVlQzuwKziupHCZMh8QgJMprn_vXh6PgClWheuFpIBmeElT6n-98pDpohIsUhNLaAZoYZRVjDljduVGfxKVipaV-UzKBLRu5VEyYNbd-nHv2vt1SCPJmJTjzmQ3qB0QRatJ4Me7VJ2DkR906Dauwme4Aai2WrChOFV3a1m886EhaKuiArBW5Og6m7hRHi7_VGsHNx-WSyTO0Dygdo_ZRW7SsMin5-C4B88XIKB_F-Q5wAvQHooVirozz2ZuFuujoEDyzHV)

## Extended functionality with `!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/common.puml`

If the common file is included, the following additional functionalities are provided per sprite:

`$Mdi<SpriteName>Img($color = $MDI_DEFAULT, $scale = "1")`: Returns the sprite as an image with the given color and scale:.
Example `MdiAccountAlertImg(red, 2)` produces an AccountAlert sprite in red with a scale factor of 2.


`$Mdi<SpriteName>($alias, $label=$MDI_DEFAULT, $shape=$MDI_DEFAULT,$color=$MDI_DEFAULT, $scale=1, $stereo=$MDI_DEFAULT)`: Returns a PlantUML element with the given alias, label, shape, color, scale and stereotype.
Example `MdiAccountAlert("myAlias", "My Label", rectangle, blue, 2, "My Stereo")` produces a blue rectangle with an AccountAlert sprite scaled by a factor of 2, the label "My Label", the alias "myAlias" and the stereotype "My Stereo".

Additionally, contains the common file some argument specific predefined constants and default values which can be changed to customize the appearance of all icons/sprites.

```plantuml
' ==========================================================
' MDI (default) values which can be used by the macros =====
'
' The default values can be overwritten before the common.puml is included
' Details of the values see below:
' !$MDI_ALIGNMENT = (""|"left"|"center"|"right")
' !$MDI_DEFAULT_LABEL = (""|"*")
' !$MDI_DEFAULT_SHAPE = ("label"|"rectangle"|...)
' !$MDI_DEFAULT_COLOR = (""|"red"|"#FF0000"|...)
' !$MDI_DEFAULT_STEREOTYPE = (""|"*"|"MDIElement"|...)
' ----------------------------------------------------------
' uses the default value which can be defined via the $MDI_DEFAULT_...=.... calls
' ($MDI_DEFAULT_LABEL, $MDI_DEFAULT_SHAPE, $MDI_DEFAULT_COLOR, $MDI_DEFAULT_STEREOTYPE)
!global $MDI_DEFAULT = "uSe_DeFaUlT"

' if no label is given don't use a label at all 
!global $MDI_LABEL_NONE = ""
' if no label is given use the alias as label 
!global $MDI_LABEL_ALIAS = "*"
!global $MDI_DEFAULT_LABEL ?= $MDI_LABEL_ALIAS

' don't display a shape (eg. rectangle) at all, around the sprite and the label
!global $MDI_SHAPE_NONE = "label"
' can be any other plantuml element too (like database, package, folder, etc.)
!global $MDI_DEFAULT_SHAPE ?= "rectangle"

!global $MDI_COLOR_NONE = ""
' can be any html color name or hex value like "red", "#FF0000", etc.
!global $MDI_DEFAULT_COLOR ?= $MDI_COLOR_NONE

' don't add a stereotype
!global $MDI_STEREOTYPE_NONE = ""
' add a stereotype with the name of the used sprite
!global $MDI_STEREOTYPE_SPRITE = "*" 
' can be any other concrete stereotype too like $MDI_DEFAULT_STEREOTYPE = "MDIElement"
' all used stereotypes/styles must be explicitly defined 
!global $MDI_DEFAULT_STEREOTYPE ?= $MDI_STEREOTYPE_NONE

' don't change the alignment of the text (label + stereotype)
!global $MDI_ALIGNMENT_NONE = ""
' left alignment of the text (label + stereotype)
!global $MDI_ALIGNMENT_LEFT = "left"
' center alignment of the text (label + stereotype)
!global $MDI_ALIGNMENT_CENTER = "center"
' right alignment of the text (label + stereotype)
!global $MDI_ALIGNMENT_RIGHT = "right"
!global $MDI_ALIGNMENT ?= $MDI_ALIGNMENT_CENTER

!if ($MDI_ALIGNMENT != $MDI_ALIGNMENT_NONE)
  skinparam defaultTextAlignment $MDI_ALIGNMENT
!endif
```

TODO: add samples from _examples_, ...


## Spites in combination with other standard libraries (e.g. C4-PlantUML)

The sprites can be used in combination with other standard libraries like C4-PlantUML too.
The usage is similar to the above described usage without additional dependencies and the sprites can be used directly as $sprite argument of the C4-PlantUML elements.

**Material sprites in combination with C4-PlantUML:**

```plantuml
@startuml

!include <C4/C4_Container>

' No common.puml loaded, text alignment remains left
'   If common.puml should be included (which is typically not required in C4 context) 
'   then any text alignment of ../common.puml can be avoided via `!$MDI_ALIGNMENT=""` 
'   before the include
' !$MDI_ALIGNMENT=""
' !include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/common.puml

!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/AccountUser/AccountAlert.puml
!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/Emoji/all.puml

package "Image sample\nwith C4" {

  Person(A, $sprite="mdiAccountAlert", $label="Person A")
  Person(B, $sprite="mdiEmoticonNeutral", $label="Person B")

  Rel(A, B, "Calls")
}

@enduml
```

[![PleaseOpenLinkIfImageCannotBeDisplayed](https://www.plantuml.com/plantuml/svg/lOz1Qzj048Nl-oic8j04Kkr542XrYQE6OcXCAUsja8obaRNDxAwwEufhIlzxHx53dUIUqoupyzxttaKMJ39wDkR8XOR7bk1zNTcwkgbZ47I1qWTZti0oGXEzZw4Sz1euOalj6GZz5a1sw-0f22JoAid0r8cA01RT4rdkuyWjh0Zsi1PEDhrhUd0PP3ku1fct4E9azMjqIGzSWBfIbp2nJk71LdeAW67xd1yxA4jxI6mmJ3YyZswYtJk4swFZwu-Bc_ddnQVbzTNoswmeRdUsA-fYeidzCP-ENrvFm_qUUf4XlxCsuQPSE-d7rPWfFQGDKceIU-TIqsVfxS0OH3EzpTAoMzb4NROzOPkjjg2W-Un-vL4eEUJpiYghyyD2nhmkUjuqSGpoNPqV_tEc9BimhvlboiUVpYBp3cu6REvmJL0i_FHaz0FJZx1HFjHL0N-C0VX2ASTmCZ-3upma9pGhVEiEgnIwObmHpuhTCSoBq__AowTA3I5EYorfb8JyKdofObL_9PwWgYvgPCuw_MlCXVRJxFy0)](https://www.plantuml.com/plantuml/uml/lOz1Qzj048Nl-oic8j04Kkr542XrYQE6OcXCAUsja8obaRNDxAwwEufhIlzxHx53dUIUqoupyzxttaKMJ39wDkR8XOR7bk1zNTcwkgbZ47I1qWTZti0oGXEzZw4Sz1euOalj6GZz5a1sw-0f22JoAid0r8cA01RT4rdkuyWjh0Zsi1PEDhrhUd0PP3ku1fct4E9azMjqIGzSWBfIbp2nJk71LdeAW67xd1yxA4jxI6mmJ3YyZswYtJk4swFZwu-Bc_ddnQVbzTNoswmeRdUsA-fYeidzCP-ENrvFm_qUUf4XlxCsuQPSE-d7rPWfFQGDKceIU-TIqsVfxS0OH3EzpTAoMzb4NROzOPkjjg2W-Un-vL4eEUJpiYghyyD2nhmkUjuqSGpoNPqV_tEc9BimhvlboiUVpYBp3cu6REvmJL0i_FHaz0FJZx1HFjHL0N-C0VX2ASTmCZ-3upma9pGhVEiEgnIwObmHpuhTCSoBq__AowTA3I5EYorfb8JyKdofObL_9PwWgYvgPCuw_MlCXVRJxFy0)

**Material sprites in combination with C4-PlantUML and its new `!NEW_C4_STYLE = 1`**

```plantuml
@startuml

' Activate new C4 style
!NEW_C4_STYLE = 1
' (stdlib <C4/C4_Container> does not yet support new C4 style, it has to be included via orig URL)
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

' No common.puml loaded, text alignment remains left
'   If common.puml should be included (which is typically not required in C4 context) 
'   then any text alignment of ../common.puml can be avoided via `!$MDI_ALIGNMENT=""` 
'   before the include
' !$MDI_ALIGNMENT=""
' !include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/common.puml

!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/AccountUser/AccountAlert.puml
!include https://raw.githubusercontent.com/kirchsth/plantuml-stdlib/refs/heads/extended/stdlib/material7.4.47/Emoji/all.puml

!$text="Image sample\nwith C4 and new Style (!NEW"+"_C4_STYLE = 1)"
package "$text" {

  Person(A, $sprite="mdiAccountAlert", $label="Person A")
  Person(B, $sprite="mdiEmoticonNeutral", $label="Person B")

  Rel(A, B, "Calls")
}

@enduml
```

[![PleaseOpenLinkIfImageCannotBeDisplayed](https://www.plantuml.com/plantuml/svg/lLDDQzj04BthLqoMG6sQI1GCWLANAAuf1iU4V50A1MSiZQrjLhlgxiYkAVtl7SasjUfJBxc9sNaVxw6v3eoUwz94qHj8CzPhP09B6nWD8F3MK7Gs6t-PZmRpXyUlqp4CuPrizWBdHY_WmsYGoDF8MKPjoN-4t540wnYsn13ggdAUEtmNe1aA3C0E5WJQPgREAOUrHd1Uh-3fVjgFplPpA9Yhy3v9F6xYbUQYNjI1V2Q2P3dEN9bK1csJu7BdIVnStZMZfzjfKc9WyXsBSRLFEtCWyDBPTWB6eTYu0AQV36ZqofQY09vAWGKmj6G10KoM7LWeN6toJfBUfj1P0Je0RokTeJ7RjX5FFshjPK7RfeqcWsZreQNbWYoWtVwhxvOGnycnOeQsaSErquVUdi_ERpzDvkbqydbsEvuz3fLwtj4kQEayDUm7Vp8-tPRXVpJ-edrM12vEglUq34b1c8T4Kf0LVyd-gKGchz5SnODuS7KSA8fULphDCbTRVXBcmtTgo7DhvfMzZ4ltNITepA69SnR4K4rAN144B2j3t-n6v9i_1ctUdj93SqVGQmvJlLMTs-ohgCBifK6hbal1hoW2k2CVdEsb5t0UAg-PXghCzN5y9Ky65sI6QhSCgUh_HTvqaMASjPGnevezcbFmZO05VK-c4HMq6adC8DFVKNGjdKZUFm00)](https://www.plantuml.com/plantuml/uml/lLDDQzj04BthLqoMG6sQI1GCWLANAAuf1iU4V50A1MSiZQrjLhlgxiYkAVtl7SasjUfJBxc9sNaVxw6v3eoUwz94qHj8CzPhP09B6nWD8F3MK7Gs6t-PZmRpXyUlqp4CuPrizWBdHY_WmsYGoDF8MKPjoN-4t540wnYsn13ggdAUEtmNe1aA3C0E5WJQPgREAOUrHd1Uh-3fVjgFplPpA9Yhy3v9F6xYbUQYNjI1V2Q2P3dEN9bK1csJu7BdIVnStZMZfzjfKc9WyXsBSRLFEtCWyDBPTWB6eTYu0AQV36ZqofQY09vAWGKmj6G10KoM7LWeN6toJfBUfj1P0Je0RokTeJ7RjX5FFshjPK7RfeqcWsZreQNbWYoWtVwhxvOGnycnOeQsaSErquVUdi_ERpzDvkbqydbsEvuz3fLwtj4kQEayDUm7Vp8-tPRXVpJ-edrM12vEglUq34b1c8T4Kf0LVyd-gKGchz5SnODuS7KSA8fULphDCbTRVXBcmtTgo7DhvfMzZ4ltNITepA69SnR4K4rAN144B2j3t-n6v9i_1ctUdj93SqVGQmvJlLMTs-ohgCBifK6hbal1hoW2k2CVdEsb5t0UAg-PXghCzN5y9Ky65sI6QhSCgUh_HTvqaMASjPGnevezcbFmZO05VK-c4HMq6adC8DFVKNGjdKZUFm00)

