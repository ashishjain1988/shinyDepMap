# shinyDepMap
A shiny-based interactive web tool to analyze [DepMap](https://depmap.org/) data (based on their 19q3 release). The website should run  [here](https://labsyspharm.shinyapps.io/depmap/), but one can download the code & data from this repository and run the tool locally.

## Preparation
To launch this tool locally, following R pacakges should be installed first.

```r
install.packages("devtools")
install.packages("BiocManager")

devtools::install_github('rstudio/flexdashboard')
devtools::install_github('hadley/ggplot2')

BiocManager::install(c("shiny", "grid","RColorBrewer","shinyWidgets","plotly","DT","visNetwork","aws.s3","tibble","dplyr","tidyr"))
```

## Run the app
Run the following commands in the directory that contains [depmap.Rmd](depmap.Rmd)
```r
library(rmarkdown)
run("depmap.Rmd")
```

## Bug reports
Please contact [me](kenichi_shimada@hms.harvard.edu) in case you find a bug.

#### Session info

	R version 3.6.1 (2019-07-05)
	Platform: x86_64-apple-darwin15.6.0 (64-bit)
	Running under: macOS High Sierra 10.13.6

	Matrix products: default
	BLAS:   /Library/Frameworks/R.framework/Versions/3.6/Resources/lib/libRblas.0.dylib
	LAPACK: /Library/Frameworks/R.framework/Versions/3.6/Resources/lib/libRlapack.dylib

	locale:
	[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

	attached base packages:
	[1] grid      stats     graphics  grDevices utils     datasets  methods  
	[8] base     

	other attached packages:
	 [1] tidyr_0.8.3           dplyr_0.8.3           tibble_2.1.3         
	 [4] aws.s3_0.3.12         visNetwork_2.0.8      DT_0.8               
	 [7] plotly_4.9.0          shinyWidgets_0.4.8    RColorBrewer_1.1-2   
	[10] ggplot2_3.2.1         flexdashboard_0.5.1.1 shiny_1.3.2          

	loaded via a namespace (and not attached):
	 [1] Rcpp_1.0.2          compiler_3.6.1      pillar_1.4.2       
	 [4] later_0.8.0         base64enc_0.1-3     tools_3.6.1        
	 [7] digest_0.6.21       viridisLite_0.3.0   jsonlite_1.6       
	[10] evaluate_0.14       gtable_0.3.0        pkgconfig_2.0.3    
	[13] rlang_0.4.0         xfun_0.9            xml2_1.2.2         
	[16] httr_1.4.1          withr_2.1.2         knitr_1.25         
	[19] htmlwidgets_1.3     tidyselect_0.2.5    data.table_1.12.2  
	[22] glue_1.3.1          R6_2.4.0            rmarkdown_1.15     
	[25] purrr_0.3.2         magrittr_1.5        scales_1.0.0       
	[28] promises_1.0.1      htmltools_0.3.6     assertthat_0.2.1   
	[31] aws.signature_0.5.2 mime_0.7            xtable_1.8-4       
	[34] colorspace_1.4-1    httpuv_1.5.2        lazyeval_0.2.2    
	[37] munsell_0.5.0       crayon_1.3.4       


