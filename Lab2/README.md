# Lab 2: Visualization using Amazon QuickSight

* [Configuring Amazon QuickSight to use Amazon Athena as data source](#configuring-amazon-quicksight-to-use-amazon-athena-as-data-source)
* [Visualizing the data using Amazon QuickSight](#visualizing-the-data-using-amazon-quicksight)
    * [Add year based filter to visualize the dataset for the year 2016](#add-year-based-filter-to-visualize-the-dataset-for-the-year-2016)
    * [Add the month based filter for the month of January](#add-the-month-based-filter-for-the-month-of-january)
    * [Visualize the data by hour of day for the month of January 2016](#visualize-the-data-by-hour-of-day-for-the-month-of-january-2016)
    * [Visualize the data for the month of January 2016 for all taxi types(yellow, green, fhv)](#visualize-the-data-for-the-month-of-january-2016-for-all-taxi-typesyellow-green-fhv)

## Architectural Diagram
![architecture-overview-lab2.png](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/architecture-overview-lab2.png)

## Visualizing the data using Amazon QuickSight

Now that you have configured the data source and created a new filed to represent the hour of the day, in this section you will filter the data by year followed by month to visualize the taxi data for the entire month of January 2016 based on the **pickup_datetime** field.

### Add year based filter to visualize the dataset for the year 2016


![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage14.PNG)

1. Ensure that current AWS region is **US West (Oregon)** region.

2. Under the **Fields List**, select the **year** field to show the distribution of fares per year.

3. To reformat the **year** without comma

   i. Select the dropdown arrow for the **year **field.

   ii. Select **Format 1,234.5678 **from the dropdown menu.

   iii. Select **1235**.

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage15.PNG)

4. To add a filter on the **year** filed, 

   i. Select the dropdown for **year** field from the **Fields list**.

   ii. Select **Add filter to the field** from the dropdown menu.

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage16.PNG)

5. To filter the data only for the year 2016

   i. Choose the new filter that you just created by clicking on **#** next to filter name **year** under the **Edit filter** menu.
  
   ii. Select **Filter list** for the two dropdowns under the filter name.
  
   iii. Deselect **Select All**.
  
   iv. Select only **2016**.
  
   v. Click **Apply**.
  
   vi. Click **Close**.

### Add the month based filter for the month of January

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage17.PNG)

1. Ensure that current AWS region is **US West(Oregon)** region.
2. Select **Visualize** from the navigation menu in the left-hand corner.
3. Under the **Fields list**, deselect **year** by clicking on **year** field name.
4. Select **month** by clicking on the **month** field name from the **Fields list**.

5. To filter the data set for the month of January (Month 1)

   i. Select the dropdown arrow for **month** field under the **Fields List**.

   ii. Select **Add filter to the field**.

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage18.PNG)

6. To filter the data for month of January 2016 (Month 1),

   i. Choose the new filter that you just created by clicking on **#** next to filter name **month** under the **Edit Filter** menu.
 
   ii. Select **Filter list** for the two dropdowns under the filter name.
 
   iii. Deselect **ALL**.
 
   iv. Select only **1**.
 
   v. Click **Apply**
 
   vi. Click **Close**.

### Visualize the data by hour of day for the month of January 2016

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage19.PNG)

1. Select **Visualize** from the navigation menu in the left-hand corner.
2. Under the **Fields list**, deselect **month** by clicking on **month** field name.
3. Select **hourofday** by clicking on the **hourofday** field name from the **Fields list**.
4. Change the visual type to a line chart by selecting the line chart icon highlighted in the screenshot below under **Visual types**.
5. Using the slider on x-axis, select the entire range [0,23] for **hourofday** field.

### Visualize the data for the month of January 2016 for all taxi types(yellow, green, fhv)

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage20.PNG)

1. Click on the double drop-down arrow underneath your username at the top-right corner of the page to reveal **X-axis**, **Value** and **Color** under **Field wells**.
2. Under the **Fields list**, deselect **hourofday** by clicking on **hourofday** field name.
3. Select **pickup_datetime** for x-axis by clicking on the **pickup_datetime **field name from **Fields list**.
4. Select **type** for Color by clicking on the **type** field name from **Fields list.**

5. Click on the field name **pickup_datetime** in x-axis to reveal a sub-menu.
6. Select **Aggregate:Day** to aggregate by day.

![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage21.PNG)
8. Using the slider on x-axis, select the entire month of January 2016 for **pickup_datetime** field.


> Note: The interesting outlier in the above graph is that on Jan23rd, 2016, you see the dip in the number of taxis across all types. Doing a quick google search for that date, gets us this weather article from NBC New York
> ![image](https://s3-us-west-2.amazonaws.com/reinvent2017content-abd313/lab2/qsimage22.PNG)

*Using Amazon QuickSight, you were able to see patterns across a time-series data by building visualizations, performing ad-hoc analysis, and quickly generating insights.*

---
## License

This library is licensed under the Apache 2.0 License. 











































