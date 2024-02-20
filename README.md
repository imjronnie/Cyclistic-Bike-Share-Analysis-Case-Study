# Cyclistic-Bike-Share-Analysis-Case-Study

## Introduction:

Welcome to the Cyclistic bike-share analysis case study! In this endeavor, I'll be taking on the role of a junior data analyst on Cyclistic's marketing team. I am excited to embark on this journey of uncovering valuable insights to drive the company's growth.

In my capacity as a junior data analyst at Cyclistic, my primary objective is to support the company's strategic goal of increasing annual memberships. This involves a meticulous examination of the behavior and preferences exhibited by two vital customer segments: casual riders and annual members. By conducting comprehensive data analysis and crafting insightful visualizations, our aim is to uncover actionable insights that will inform the development of a targeted marketing approach, specifically tailored to convert casual riders into loyal annual members. Following the structured framework of the six phases in the data analysis process, our ultimate aim is to deliver compelling recommendations backed by robust data, thereby securing buy-in from Cyclistic's executives. Through this process, we aspire to propel Cyclistic towards its overarching vision of becoming a trailblazer in urban mobility, championing sustainable transportation practices within Chicago's vibrant bike-sharing ecosystem.

## Background — About the Company:

Picture this: Cyclistic, a bike-share program with a whopping 5,800 bicycles and 600 docking stations, cruising the streets of Chicago. What sets it apart? Inclusivity. We're not just about regular bikes – we've got reclining bikes, hand tricycles, and cargo bikes, catering to everyone, including folks with disabilities. Most riders go for the classic bikes, but 8% love the assistive options. Whether it's a leisurely ride or a daily commute, Cyclistic is the go-to.

## ASK

Three questions will guide the future marketing program: 

  1. How do annual members and casual riders use Cyclistic bikes differently? 

  2. Why would casual riders buy Cyclistic annual memberships? 

  3. How can Cyclistic use digital media to influence casual riders to become members?

## Characters & Teams:

  <b>Lily Moreno:</b> The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. These may include email, social media, and other channels.

  <b>Cyclistic Executive Team:</b> A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy learning about Cyclistic’s mission and business goals—as well as how you, as a junior data analyst, can help Cyclistic achieve them.


  <b>Cyclistic Marketing Analytics Team:</b> The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program  

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
