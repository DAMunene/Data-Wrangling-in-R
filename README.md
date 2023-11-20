# Data-Wrangling-in-R
#Install and Load Packages
install.packages("dplyr")
install.packages("tidyr")
library(dplyr)
library(tidyr)
# Example assuming a CSV file
data <- read.csv("your_data.csv")
#Explore data
head(data)
summary(data)
str(data)
#Select Columns (dplyr::select)
data_select <- select(data, column1, column2)
#Filter Rows (dplyr::filter)
data_filtered <- filter(data, column1 > 10)
#Arrange Rows (dplyr::arrange):
data_sorted <- arrange(data, column1)
#Create New Variables (dplyr::mutate)
data_mutated <- mutate(data, new_column = column1 * 2)
#Handle Missing Values (tidyr::drop_na)
data_clean <- drop_na(data)
#Reshape Data (tidyr::gather and tidyr::spread)
data_long <- gather(data, key = "variable", value = "value", -id)
data_wide <- spread(data_long, key = "variable", value = "value")
#Group and Summarize (dplyr::group_by and dplyr::summarize)
data_summarized <- data %>%
  group_by(grouping_column) %>%
  summarize(mean_value = mean(value))
#Join Data Frames (dplyr::left_join, dplyr::inner_join, etc.)
data_combined <- left_join(data1, data2, by = "common_column")




