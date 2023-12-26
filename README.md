# Cyclistic-Bike-Share-Analysis-Case-Study

## Introduction:

Greetings! In this exciting Cyclistic bike-share analysis, I, a junior data analyst at Cyclistic in Chicago, delve into the intriguing world of user behavior. The mission? Uncover how annual members and casual riders interact with Cyclistic bikes differently. The end goal? Craft a killer marketing strategy to turn those casual riders into long-term annual members. Get ready to tag along on this data-driven adventure as we navigate real-world challenges and collaborate with Cyclistic's dynamic team.

## Background — About the Company:

Picture this: Cyclistic, a bike-share program with a whopping 5,800 bicycles and 600 docking stations, cruising the streets of Chicago. What sets it apart? Inclusivity. We're not just about regular bikes – we've got reclining bikes, hand tricycles, and cargo bikes, catering to everyone, including folks with disabilities. Most riders go for the classic bikes, but 8% love the assistive options. Whether it's a leisurely ride or a daily commute, Cyclistic is the go-to.

## Business Task — Marketing Strategy:

Here's the deal: our annual membership numbers are stuck. Lily Moreno, our marketing guru, wants answers. My job? Figure out how casual riders and annual members are different. Why? So we can cook up a genius marketing plan to turn casual riders into annual members. But wait, there's a catch – the big shots at Cyclistic need to give the nod. That means my recommendations better be backed by data wizardry and slick visualizations. The plan? Dive deep into Cyclistic's historical bike trip data, spot trends, and unveil the secrets of our riders. Let's craft a strategy that not only makes sense but also propels Cyclistic to new heights. Stick around for a journey through data, insights, and the makings of Cyclistic's future success.

## Prepare Data

#### Code for combining 11 CSV files into one in R
```r
library(data.table)

# Local directory path where CSV files are stored
file_path <- "F:/Root-Portfolio Projects/Google Data Analyst Capstone Project/Cyclistic Bike-Share Analysis"

# To get a list of all CSV files in the directory
csv_files <- list.files(path = file_path, pattern = "\\.csv$", full.names = TRUE)

# Read and combine all CSV files into one data.table
cyclistic_bike <- rbindlist(lapply(csv_files, fread))

# Save the combined data to a new CSV file
write.csv(cyclistic_bike, file = "F:/Root-Portfolio Projects/Google Data Analyst Capstone Project/Cyclistic Bike-Share Analysis/cyclistic_bike.csv", row.names = FALSE)
```
