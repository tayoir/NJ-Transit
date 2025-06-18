This project focuses on data analysis of 27 months of New Jersey Transit commuter train data, from March 2018 to May 2020, covering roughly 1000 daily trains across 167 stations. Each train contains 11 variables, including date, route number, stop sequence, origin and destination names and ID numbers, scheduled and actual time, and delays.

First, the data is scraped to a large CSV file at which point it’s processed into a data frame. Next, a time table is generated through use of python’s unique() function to isolate train numbers.


<p align="center">
<img width="362" alt="Screenshot 2025-06-18 at 12 45 20 PM" src="https://github.com/user-attachments/assets/645f1580-6539-4477-ab46-4380c3fc311a" />

**<p align="center">
Timetable sample showing train number, origin, and destination. The data includes a total of 842 unique train routes.**

Next, the code takes input to identify a route by train number and provides mean and median lateness values. Mean and median delays are compared to account for occasional extreme delays on certain routes. The Straggler’s Guide shows probability of making a train given various lateness intervals at each station along a route.



![mean-mediancomparison](https://github.com/user-attachments/assets/c38e75f2-db59-46a7-afda-94f9fbb6a6da)

**<p align="center">
Comparison of mean and median delays by station for train 3805. Note the skew caused by extreme delays near the origin and destination stations where median delays are zero.**




![odds](https://github.com/user-attachments/assets/dcfbd635-7c9a-449a-be5b-cc75f640fbe8)

**<p align="center">
Likelihood of making a train given 1, 3, 5, 10, and 15 minute lateness by station.**

The Straggler’s Tool builds on the guide, asking users for their train, number departure station, and (honest) lateness before providing them with a likelihood of catching the train. It also provides a visual of their standing within the distribution of lateness for their train at that station.



<p align="center">
<img width="500" alt="Screenshot 2025-06-18 at 1 42 32 PM" src="https://github.com/user-attachments/assets/3d42b121-0a33-4a88-af78-e311c386924c" />

![histo](https://github.com/user-attachments/assets/caad06e6-b86e-4154-893d-ccfe88f4934e)

**<p align="center">
Example Straggler's Tool dialogue (top) and visual (bottom).**

Next, the code uses dictionaries to compare the overall efficiency of different stations. Each station has its largest train per day value calculated and compared with its mean delay time. Stations with many trains and a low mean delay are deemed more efficient.



![station](https://github.com/user-attachments/assets/01746cee-e0c8-4352-b247-3ead16cb397b)
**<p align="center">
Station efficiency visualization with outliers noted.**


The dataset is too large to attach entirely but a sample is included and the full set is available online. Also attached is a PDF presentation and the JuPyTer notebook file used as a project workspace. Feel free to reach out with any questions/comments to tayoilungareed@gmail.com. [NEW JERSEY TRANSIT IS THE ABSOLUTE WORST!](https://www.youtube.com/watch?v=gpvGZy-kM-c)


