# Income Replacement Ratio Calculator

## Overview

The **Income Replacement Ratio (IRR) Calculator** is a Shiny-based tool designed to help users estimate the percentage of their pre-retirement income they will need to replace during retirement. The calculator gathers user inputs such as current age, retirement age, salary, contributions, expected retirement income streams (e.g., Social Security, pension, and savings withdrawals), and assumptions on tax and inflation rates. It then computes the projected retirement income and compares it to the desired income replacement ratio, displaying the results along with a progress bar and a descriptive message indicating whether the income replacement is "Insufficient", "Adequate", or "Sufficient".

## Features

- **User-Friendly Interface:** Input fields with tooltips to guide users through providing necessary details.
- **Dynamic Calculations:** Computes key metrics including annual income, total retirement income, after-tax income, inflation adjustments, and income shortfall.
- **Visual Feedback:** Displays a progress bar with a descriptive message based on the calculated income replacement ratio.
- **Customization:** All monetary values are formatted in Kenyan Shillings (KES).
- **Responsive Design:** The interface scrolls to the results section once the computation is complete for an improved user experience.
- **Disclaimer:** Includes a clear disclaimer advising users to consult a financial adviser for personalized advice.

## Project Structure

- **UI Module (`irrCalcUI`):** Contains the user interface elements, including input fields and output areas, organized into several fluid rows and boxes.
- **Server Module (`irrCalcServer`):** Handles the computation logic, progress updates, and dynamic UI rendering for the results.
- **Customization:** The project displays monetary values in KES rather than USD, and uses the `scales::dollar` function with a KES prefix.


## Technologies Used

- **R** - Programming language for statistical computing and graphics.
- **Shiny** - An R package for building interactive web applications.
- **bs4Dash** - A modern dashboard framework based on Bootstrap 4.
- **ggplot2** - For creating elegant graphics for data visualization.
- **bslib** - For theming Shiny applications.
- **plotly** - For interactive plotting.
- **DT** - For rendering data tables in Shiny.
- **dplyr** - For data manipulation.
- **lubridate** - For easy manipulation of dates and times.

## Installation

To run this application locally, you need to have R installed along with the following R packages:

```R
install.packages(c("shiny", "bs4Dash", "ggplot2", "bslib", "plotly", "DT", "dplyr", "lubridate"))
```

## Usage

### Input Fields:
- Fill in your details such as your name, current age, retirement age, monthly salary (in KES), and various retirement assumptions.

### Calculation Process:
The IRR Calculator will compute:
- **Annual pre-retirement income.**
- **Total retirement income** from Social Security, pension, and savings withdrawals.
- **Tax adjustments and inflation adjustments.**
- **A final comparison** between your desired income replacement and the computed after-tax income.

### Results Display:
The output includes:
- A title message summarizing your retirement income status.
- An unordered list detailing key financial metrics.
- A progress bar along with a descriptive statement (e.g., "Your Income Replacement Ratio is Adequate: 75%").
