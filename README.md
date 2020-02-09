---
title: "Dataviz"
author: "Chenming Ran"
date: "2/8/2020"
output: html_document
editor_options: 
  chunk_output_type: console
---
```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
knitr::opts_chunk$set(message = FALSE)
```


```{r load-packages, message = FALSE}
library(tidyverse)
library(haven)
```

```{r import data, message = FALSE}
import <- read_stata("us_import.dta")
```

```{r summarize data, message = FALSE}
import %>%
  group_by(year) %>%
  summarize(tot_imp = mean(tot_imp)) 
```

