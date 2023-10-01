## Design a Data Dashboard Final project - by Shashank Salian


### Topic: Top Level dashboard for Super Store Dataset

#### A.  Dashboard Link: https://public.tableau.com/app/profile/shashank.s4018/viz/Superstore_Dashboard_Prototype/Top_Level_Dashboard?publish=yes
  
#### B.  New Tableau Concept learned and applied:


##### Parametric fields:


I created a parametric field called Performance_Metric:

Then I created a measured field with the same name i.e. Performance_Metric:
with the calculation logic as follows:


if [Parameters].[Performance_Metric] = "Sales" then sum([sales])\
ELSEIF [Parameters].[Performance_Metric] = "Quantity" then sum([Quantity])\
ELSEIF [Parameters].[Performance_Metric] = "Profit" then sum([profit])\
ELSE avg([Profit Ratio]) end


Using the above I created a new filter:

One could also find a discussion thread related to parametric field here:
(https://community.tableau.com/s/question/0D54T00000C5uekSAB/can-we-show-and-select-measures-and-dimension-in-control-box-list-box-or-drop-down-box)


#### C. How to use filters?


Order Year:
Selecting a year changes the Top-Level performance chart and Sub-category charts. 
The Year on Year segment performance line chart (bottom left) remains unchanged 
since it plots across all the years (i.e. 2015,2016,2017,2018) .


Performance Metric:
Selecting a performance metric from the dropdown
dynamically updates all the three charts as per the selected performance metric.


Sub-Category:


Selecting sub-categories updates the metrics in all the three charts based on 
selected sub-category. (i.e. at sub-category level and also overall segment level).


#### D. Design Choices:


##### Colorblind palette:

##### Visual encodings:
Use of length and shade  as encodings to highlight higher performing 
sub-categories for each segment.

##### Text hierarchy:
Main title and and the chart title use same color scheme and title is emphasised with larger font-size.

##### Data source info:
Data source information added at bottom of the dashboard.


