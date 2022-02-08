# set up libraries
library(wesanderson)
library(kableExtra)
library(opendatatoronto)
library(dplyr)
library(haven)
library(tidyverse)
library(corrplot)
library(ggplot2)
library(ggpubr)

# get package from open data Toronto
package <- show_package("ac77f532-f18b-427c-905c-4ae87ce69c93")
package
# get all resources for this package
resources <- list_package_resources("ac77f532-f18b-427c-905c-4ae87ce69c93")
# identify datastore resources; by default, Toronto Open Data sets datastore resource format to CSV for non-geospatial and GeoJSON for geospatial resources
datastore_resources <- filter(resources, tolower(format) %in% c('csv', 'geojson'))
# load the first datastore resource as a sample
data <- filter(datastore_resources, row_number()==1) %>% get_resource()
data
