# Cyclistic-Bike-Share-Analysis-Case-Study

## Prepare Data

#### Code for combining 11 csv file into one in R
```r
library(data.table)

# Directory path where your CSV files are located
file_path <- "F:/Root-Portfolio Projects/Google Data Analyst Capstone Project/Cyclistic Bike-Share Analysis"

# Get a list of all CSV files in the directory
csv_files <- list.files(path = file_path, pattern = "\\.csv$", full.names = TRUE)

# Read and combine all CSV files into one data.table
cyclistic_bike <- rbindlist(lapply(csv_files, fread))

# Save the combined data to a new CSV file
write.csv(cyclistic_bike, file = "F:/Root-Portfolio Projects/Google Data Analyst Capstone Project/Cyclistic Bike-Share Analysis/cyclistic_bike.csv", row.names = FALSE)

# Print a message indicating success
print("CSV files combined and saved as 'combined_data.csv'")
```
