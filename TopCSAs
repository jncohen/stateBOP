# Generate Top CSAs by Population Using Census Data
# Link: http://www.josephnathancohen.info/notes/combined-statistical-areas/

# Clear Memory
rm(list=ls())
gc()

# Set Working Directory
# Substitute your.directory for path
your.directory <- ""
setwd(your.directory)

# Load data from public-distribution CSV
data <- read.csv("csa-est2019-alldata.csv") 

# Narrow set to CSAs
data <- subset(data, LSAD == "Combined Statistical Area")[c(5,18)]

# Sort in descending order
library(dplyr)
data <- arrange(data, -POPESTIMATE2019)

# Format Population Column
data[2] <- format(data[2], big.mark=",")

# Generate Table
library(kableExtra)
kable(data[1:10,]) %>%
  kable_styling()
