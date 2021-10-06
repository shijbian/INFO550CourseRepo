## INFO 550 Project

This is the repo for INFO550 project in Fall 2021

To knit the R Markdown file, you need the packages below:

```r
knitr::opts_chunk$set(echo = TRUE)
installed_pkgs <- row.names(installed.packages())
pkgs <- c("tidyverse", "oro.dicom")
for(p in pkgs){
	if(!(p %in% installed_pkgs)){
		install.packages(p)
	}
}

library(tidyverse)
library(oro.dicom)
```

Depending which directory you pull *INFO550CourseRepo*, to run this R Markdown file, remeber to re-set the path to this repo *INFO550CourseRepo* in the R markdown file at Line 28:

```r
data_path <- c("~/Dropbox/Emory Courses/Fall 2021/INFO 550/github_repo/INFO550CourseRepo/")
```

## Execute the analysis

To execute the analysis, from the project folder /INFO550CourseRepo/Script/ you can run 

``` bash
Rscript -e "rmarkdown::render('Sep22_2021.Rmd')"   
```

This will create a file called `Sep22_2021.html` output in your directory that contains the results.

## Data
The data used in this project is provided by Kaggle competition "[RSNA-MICCAI Brain Tumor
Radiogenomic Classification](https://www.kaggle.com/c/rsna-miccai-brain-tumor-radiogenomic-classification/overview)".

