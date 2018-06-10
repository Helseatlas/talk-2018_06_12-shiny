name: blank
layout: true

---
name: reduced
layout: true
class: left
background-image: url(bg_wide_reduced.png)


---
name: front
layout: true
class: center, middle
background-image: url(bg_front_wide.png)

---
name: normal
layout: true
class: left
background-image: url(bg_wide.png)

---
template: front

.title[RShiny ved SKDE]

.subtitle[Bruk og erfaringer]

.author[Arnfinn Hykkerud Steindal]

---
template: front

# Tabellverket

.footnote[[https://skde.shinyapps.io/tabellverk](https://skde.shinyapps.io/tabellverk)]

---
template: blank

<iframe src="https://skde.shinyapps.io/tabellverk/" style="height:550px;width:1050px;">Tabellverk </iframe>

[https://skde.shinyapps.io/tabellverk](https://skde.shinyapps.io/tabellverk)

---
template: blank

<iframe src="https://skde.shinyapps.io/iframe" style="height:550px;width:1050px;">Tabellverk </iframe>

[https://skde.shinyapps.io/iframe](https://skde.shinyapps.io/iframe)

---
template: front

# R-pakke

---
template: normal

# R-pakke

.left-column[
## Hvorfor?
]

.right-column[
### Skiller data fra kode
###  Kan enkelt brukes på flere prosjekter
###  Kan testes

]

---
template: normal

# R-pakke

.left-column[
## Splitt data og kode
]


.right-column[
```R
# Installer pakke
devtools::install_github("Helseatlas/shinymap")
# Les inn helseatlas-data
mydata <- readRDS("data.rds")
# Kart
kartdata <- "<some-map-file>"
# Send opp til shinyapp.io
shinymap::submit_application(dataset = mydata, name = "kols", map = kartdata, ...)
```
]

---
template: normal

# R-pakke

.left-column[
## Innhold i pakken
]

.right-column[
```
R/
  launch_application.R
data/
     kols.RData
inst/
     app/
         server.R 
         ui.R
         www/
man/
    create_appDir.Rd
    launch_application.Rd
    submit_application.Rd
tests/
      testthat.R
      testthat/
               data/
               test_launch.R
.Rbuildignore
.gitignore
.travis.yml
DESCRIPTION
LICENSE
NAMESPACE
README.md
```
]

---
# Git og Github





---
template: reduced

# `git` i RStudio

.left-column[

]


.right-column[

.right[![Right-aligned image](fig/git_rstudio.png)]

]







