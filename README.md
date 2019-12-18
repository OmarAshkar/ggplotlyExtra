
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ggplotlyExtra

<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/ggplotlyExtra)](https://CRAN.R-project.org/package=ggplotlyExtra)
<!-- badges: end -->

The goal of ggplotlyExtra is to make a ready-customized functions for
smooth transition between ‘ggplot2’ and ‘plotly’.

## Installation

You can install the released version of ggplotlyExtra from
[CRAN](https://cran.r-project.org/web/packages/ggplotlyExtra/index.html)
with:

``` r
install.packages("ggplotlyExtra")
```

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("omarelashkar/ggplotlyExtra")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(ggplot2)
library(plotly)
#> 
#> Attaching package: 'plotly'
#> The following object is masked from 'package:ggplot2':
#> 
#>     last_plot
#> The following object is masked from 'package:stats':
#> 
#>     filter
#> The following object is masked from 'package:graphics':
#> 
#>     layout
library(ggplotlyExtra)

p <- ggplot() + 
        ggplotly_histogram(data = ToothGrowth, mapping = aes(len)) +
        xlab("len")
#> `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
#> Warning: Ignoring unknown aesthetics: label1, label2, label3

ggplotly(p, tooltip = c("Range", "count", "density"))
#> PhantomJS not found. You can install it with webshot::install_phantomjs(). If it is installed, please make sure the phantomjs executable can be found via the PATH variable.
```

<!--html_preserve-->

<div id="htmlwidget-4291228f7573a083622c" class="plotly html-widget" style="width:100%;height:480px;">

</div>

<script type="application/json" data-for="htmlwidget-4291228f7573a083622c">{"x":{"data":[{"orientation":"v","width":[1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],"base":[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],"x":[4.09655172413793,5.12068965517241,6.1448275862069,7.16896551724138,8.19310344827586,9.21724137931034,10.2413793103448,11.2655172413793,12.2896551724138,13.3137931034483,14.3379310344828,15.3620689655172,16.3862068965517,17.4103448275862,18.4344827586207,19.4586206896552,20.4827586206897,21.5068965517241,22.5310344827586,23.5551724137931,24.5793103448276,25.6034482758621,26.6275862068965,27.651724137931,28.6758620689655,29.7,30.7241379310345,31.748275862069,32.7724137931034,33.7965517241379],"y":[1,1,2,2,1,3,2,3,0,1,3,3,3,3,2,1,1,3,3,4,2,4,5,2,0,2,1,0,1,1],"text":"","type":"bar","marker":{"autocolorscale":false,"color":"rgba(89,89,89,1)","line":{"width":1.88976377952756,"color":"transparent"}},"showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":31.4155251141553},"plot_bgcolor":"rgba(235,235,235,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[2.06155172413793,35.8315517241379],"tickmode":"array","ticktext":["10","20","30"],"tickvals":[10,20,30],"categoryorder":"array","categoryarray":["10","20","30"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"y","title":{"text":"len","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[-0.25,5.25],"tickmode":"array","ticktext":["0","1","2","3","4","5"],"tickvals":[0,1,2,3,4,5],"categoryorder":"array","categoryarray":["0","1","2","3","4","5"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"x","title":{"text":".data$count","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":null,"line":{"color":null,"width":0,"linetype":[]},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":false,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895}},"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","showSendToCloud":false},"source":"A","attrs":{"4c7e3a5f2b8a":{"x":{},"y":{},"label1":{},"label2":{},"label3":{},"type":"bar"}},"cur_data":"4c7e3a5f2b8a","visdat":{"4c7e3a5f2b8a":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

<!--/html_preserve-->
