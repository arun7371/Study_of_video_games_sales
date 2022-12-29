# Study_of_video_games_sales
Videogame sales were the subject of this case study. The dataset was downloaded from the Kaggle website. The dataset contains a list of video games that have sold more than 100,000 copies. In order to clean and reshape the data, I used Microsoft Excel, and then I visualized it using Microsoft PowerBi.

Fields includes :

Rank - Ranking of overall sales

Name - The games name

Platform - Platform of the games release (i.e. PC,PS4, etc.)

Year - Year of the game's release

Genre - Genre of the game

Publisher - Publisher of the game

NA_Sales - Sales in North America (in millions)

EU_Sales - Sales in Europe (in millions)

JP_Sales - Sales in Japan (in millions)

Other_Sales - Sales in the rest of the world (in millions)

Global_Sales - Total worldwide sales. (in millions)


Let's get started :-)

1) First we need to pull the csv file to excel or to powerBi for data cleaning process

2) Check the datatype of each column  

3) As I said before this dataset has been download from kaggle, usaully the dataset from kaggle does not have mismatches or data errors so thanks to GregorySmith (Owner) of the dataset.

4) So we can straight away jump to data reshaping. NA_Sales - Sales in North America (in millions) but the actual value in cell will not be in million so we need to multiple the actual value * 10^7 to get the value in million this should done for following columns 
NA_Sales - Sales in North America (in millions)

EU_Sales - Sales in Europe (in millions)

JP_Sales - Sales in Japan (in millions)

Other_Sales - Sales in the rest of the world (in millions)

Global_Sales - Total worldwide sales. (in millions)
![inmillions](https://user-images.githubusercontent.com/86791724/209925432-7ae583c5-9698-41fc-90a6-e8e95b1b9be5.PNG)

5) Once we convert the value to millions we can simply convert them into currency 

6) To create a detailed data praticularly on Genre we need to find the distinct value, count and contribution of individual genre in video games

7) To find the count of each genre we could simply use the countif formula

8) To find the percentage of each gerne we need to compute count of each (genre/ sum(count of each gerne)) WE can also use the measure if we use powerBi to transform data. 
the gerne detail table looks like

![Genre_detail_table](https://user-images.githubusercontent.com/86791724/209925797-c7c1db21-429a-4b9a-89e3-e141bae56afc.PNG)


9) Now it's time to get the data in PowerBi, To pull the data in PowerBi click the getdata it will show text/csv file click and goto the the file destination the get the data.

10) It will ask to load or transform the data. click the transform, Once again we might check the datatype of the respective column.

11) Once we finished the checking click the close and apply which will present in the left top side. This will load the data

12) Goto manage relation or model (Which is thrid option). This is very important step we need to relate the table to other table (It's very much similar to the JOIN in SQL) The genre_detail table will be connected to the vgsales table (1 to *)
![Relationship](https://user-images.githubusercontent.com/86791724/209925643-da63a5a2-78ef-4147-af82-c73c0d307934.PNG)


13)  Now we are finally ready to create the report :-)
![page_1](https://user-images.githubusercontent.com/86791724/209925527-4923733e-2774-42a6-9262-ea17a92af1ee.PNG)

![page_2](https://user-images.githubusercontent.com/86791724/209925542-f9f38df9-79d9-490a-9b8f-245e332b5d6c.PNG)

![page_3](https://user-images.githubusercontent.com/86791724/209925550-7df32bcc-ff4c-4991-9316-5857295a4178.PNG)

![page_4](https://user-images.githubusercontent.com/86791724/209925558-b38e4256-26a7-46c7-a63f-ecc8e74cbf86.PNG)




