# SharePoint Budget Monitoring with Power BI and Power Automate

This project demonstrates an end-to-end process of monitoring budget data through a SharePoint list, visualizing the data using Power BI, and automating notifications with Power Automate when certain conditions are met (e.g., budget thresholds exceeded).
Overview

The central component of this project is a SharePoint list that contains budget data. This list is connected to a Power BI report to provide real-time data visualization and analytics. An automated workflow using Power Automate triggers when specific conditions in the data are satisfied, such as when the actual spending exceeds the budgeted amount. This trigger sends an email notification to a designated user.
Project Structure

    SharePoint List: Contains columns for budget categories, planned amount, actual spending, etc.
    Power BI Report: Visualizes data from the SharePoint list, highlighting key metrics and trends.
    Power Automate Flow: Monitors the output of a query run against the Power BI dataset and sends an email if a specified condition (e.g., budget exceeded) is true.

Set Up and Configuration
SharePoint

    Create a SharePoint List:
        Navigate to your SharePoint site and create a new list.
        Define necessary columns for budget tracking, such as Category, BudgetedAmount, ActualAmount.

Power BI

    Connect Power BI to the SharePoint List:
        Open Power BI Desktop.
        Select Get Data > More > Online Services > SharePoint Online List.
        Provide the URL of your SharePoint site and select the list you created.

    Create the Power BI Report:
        Build visuals that compare BudgetedAmount and ActualAmount.
        Publish this report to the Power BI Service.

Power Automate

    Set up the Power Automate Flow:
        Trigger: Schedule or set an appropriate trigger.
        Action: Use "Run a query against a dataset" to fetch the latest data from your Power BI report.
        Condition: Check if any budget category has exceeded its limit.
        Action: Send an email notification if the condition is true.
