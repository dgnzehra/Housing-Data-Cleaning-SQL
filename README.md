# Nashville Housing Data Cleaning in SQL

## Overview

This SQL project focuses on cleaning and enhancing Nashville housing data for improved analysis. The dataset, obtained from [https://www.kaggle.com/datasets/tmthyjames/nashville-housing-data], includes information on real estate properties in Nashville. The provided SQL script outlines the steps taken to refine the dataset, addressing issues such as standardizing data formats, populating missing property addresses, breaking down addresses into individual columns, and transforming categorical values. The ultimate goal is to provide a cleansed dataset that facilitates more accurate and insightful data analysis.

## Data Cleaning Steps

### Standardizing Data Format

The script begins by standardizing the date format in the `SaleDate` column to ensure consistency for further analysis. The original data is transformed into a cleaner and more uniform structure.

### Populating Property Address Data

To address missing property addresses, the script utilizes data from other records with the same `ParcelID`. This process involves identifying and updating records where the `PropertyAddress` is null, improving the overall completeness of the dataset.

### Breaking out Address into Individual Columns

The `PropertyAddress` field is broken down into individual columns, including `Address`, `City`, and `State`. This enhances the granularity of location data and facilitates more detailed spatial analysis.

### Breaking out Owner Address into Individual Columns

Similar to property addresses, the script breaks down `OwnerAddress` into individual columns for `Address`, `City`, and `State`. This transformation provides a clearer representation of owner location details.

### Change 'Y' and 'N' to 'Yes' and 'No' in "Sold as Vacant" Field

The script updates the values in the `SoldAsVacant` field, changing 'Y' to 'Yes' and 'N' to 'No'. This enhances clarity and consistency in the representation of vacant property sales.

### Removing Duplicates

Duplicate records are identified and removed based on specific criteria, ensuring data integrity and preventing redundancy in the dataset.

### Delete Unused Columns

Unnecessary columns such as `OwnerAddress`, `TaxDistrict`, `PropertyAddress`, and `SaleDate` are removed from the dataset, streamlining it for more focused analysis.
