# Time_Series_Forecasting_With_Prophet

In this project, I've took advantage from these 
* [Part-1](https://youtu.be/hht0iKzviWE?si=xlIO_hD5z1QQ4Nrt) and
* [Part-2](https://youtu.be/CLHlGbu5YaI?si=6x9I1BJMcmI4q4AE) cover each steps and more. 

The majority of this notebook is from Part 1, but I have also included some code and more from Part 2. I did not follow the "HYPERPARAMETER TUNING AND BACKTESTING" instructions in Part 2. However, cross validation techniques were used without hyperparameters from Part 1. 

If you are confused, you can check out the sources or contact me. Also, please keep in mind that I am still learning, so if you spot any incorrect explanations or anything, please let me know. Enjoy your journey, as well.


In addition, I've added my personal comments and tried some different methods for reaching results.

---
In general, in this notebook, we've worked on the "store sales" dataset, which is sales data for the Ecuador retail brand. And the dataset includes different sheets. In this notebook, we focused on the train.csv dataset. The train.csv dataset includes id, date, store number, family (the main category for sales), sales (sales price), and onpromotion columns. Before training our model, we prepared our dataset for the Prophet model. Firstly, we grouped our data first by date, then we grouped second time for family (category). And as a last thing, we calculated the sum of each day's family sales.

And then we created a new pivot table for readability. Then we filtered our data into different datasets after 2015-08-15. Because of the clearer data.

For focusing on most volume families (categories), we split three datasets into low, mid, and high volume datasets.

And then we selected our target family from a high-volume dataset as a "product" category. Later on, we created a holiday dataset, which is getting holiday dates from the "holidays" library for ECUADOR. Before creating our model, The last thing we decided was to exclude the last 30 days as a test dataset. and determined the period to be 30 days.

We select the FACEOOK PROPHET model for our time series.
* determined period as 30 days.
* calculated model's MAPE.

Model evaluation with the cross-validation method.
