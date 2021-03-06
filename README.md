# rVega: An R wrapper for Vega

Created by Thomas Reinholdsson (<reinholdsson@gmail.com>).

Shiny demo: [http://glimmer.rstudio.com/reinholdsson/rVega-treemap/](http://glimmer.rstudio.com/reinholdsson/rVega-treemap/).

More about Vega: [http://trifacta.github.com/vega/](http://trifacta.github.com/vega/).

## Installation

    devtools::install_github("rVega", "metagraf")

## Examples

```
library(rVega)
vega_treemap(1:26, letters)
```

=> Live demo: [http://glimmer.rstudio.com/reinholdsson/rVega-demo-1/](http://glimmer.rstudio.com/reinholdsson/rVega-demo-1/)

## Use with Shiny

#### server.R
```
library(rVega)
shinyServer(function(input, output) {
    output$treemap <- renderVega({
        vega_treemap(1:26, letters)
    })
})
```

#### ui.R
```
library(rVega)
shinyUI(bootstrapPage(
    vegaOutput("treemap")
))
```

## See also

- [gg2v](https://github.com/hadley/gg2v) by Hadley Wickham

- [clickme](https://github.com/nachocab/clickme) by Nacho Caballero





