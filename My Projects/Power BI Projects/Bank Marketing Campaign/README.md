# Power BI Project: Bank Marketing Dataset

## Project Overview

**Project Title**: Bank Marketing Analysis  
**Objective**:  
To analyze a bank marketing dataset using Power BI to gain insights into customer behavior, optimize marketing efforts, and identify key trends affecting client subscriptions to term deposits.

**Dataset Summary**:  
- **Source**: [Bank Marketing Dataset on Kaggle](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)  
- **Size**: 17 columns, 45,211 rows  
- **Key Features**: Customer demographics, campaign contact information, and campaign outcomes (success or failure).

## Objectives

- To create an interactive and informative Power BI dashboard.
- To analyze client demographics, campaign success, and predict future outcomes.
- To provide actionable insights for optimizing marketing strategies.

## Data Preparation

1. **Data Cleaning**:
   - Removed duplicates and irrelevant columns.
   - Handled missing values in categorical and numerical columns.
   - Converted data types where necessary.

2. **Calculated Columns**:
   - **Deposit_Subscribed**: Converted `deposit` to binary (`1` for "yes", `0` for "no").
   - **Age_Group**: Categorized `age` into groups ("under 30", "30-39", "40-49", "50-59", "60 and above").
   - **ContactMonthGroup**: Grouped by contact month.
   - **DurationMinutes**: Converted `duration` from seconds to minutes.
   - **Is_Recontacted**: Indicator if a client was previously contacted.

3. **DAX Measures**:
   - **Campaign Success Rate**:
     ```DAX
     CampaignSuccessRate = 
     DIVIDE(
         CALCULATE(COUNTROWS(bank), bank[Deposit_Subscribed] = 1),
         COUNTROWS(bank),
         0
     )
     ```

## Visualizations

1. **Page 1: Overview Dashboard**:
   - **KPI Cards**:
     - Total Campaign Contacts
     - Average Balance
     - Campaign Success Rate
   - **Column Chart**: Campaign success rate by month.

2. **Page 2: Predictive Analysis and Patterns**:
   - **Forecasting**: Used for predicting future campaign outcomes.
   - **Heatmap**: Analyzes client characteristics and success patterns.

## Insights

- **Monthly Trends**: Higher subscription rates are observed during specific months.
- **Age Groups**: Clients aged `30-39` and `40-49` are more likely to subscribe.
- **Loans Impact**: Personal and housing loans influence the likelihood of subscription.

## Contributing

Feel free to fork the repository and submit pull requests. For major changes or feature requests, please open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or inquiries, please contact me at:
- **Email**: [z.amr80@gmail.com](mailto:z.amr80@gmail.com)
- **LinkedIn**: [Amr Zaki](https://www.linkedin.com/in/amr-zaki-/)
- **GitHub**: [Amr Zaki Data](https://github.com/amr-zaki-data)
