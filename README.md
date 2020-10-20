# Data Analysis of No-show Medical Appointments

### Goal 
To perform exploratory data analysis of No-show appointments using Python's pandas and Numpy packages in Jupyter Notebook. 

### Dataset
noshowappointments-kagglev2-may-2016.csv contains all information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. 

Following research questions were selected for this project.
1. What factors are important for us to know if a patient will show up for their scheduled appointment?
2. Do patients show up more if appointments are scheduled on weekends or weekdays?
3. Does waiting time i.e. ScheduledDay - AppointmentDay lead to no shows?

Project2_Investiigate_a_dataset.html file contains a detailed analysis of my work. 

### Data Wrangling
* Prior to performing exploratory data analysis, I wrangled the data to get it ready for analysis. 
* I created a box plot for Age column to determine outliers in the dataset and eliminated those rows. ScheduledDay and AppointmentDay columns were converted to date time format. 
* Handcap column initially had 5 distinct values (0, 1, 2, 3, 4, 5) and were later converted to a binary value (0 and 1)
* Age_group column was added that grouped patients in the following categories:
    0 - 12 : Child <br/>
    13 - 19 : Teenager <br/>
    20 - 30 : Young Adult <br/>
    31- 60: Adults <br/>
    grater than 60 : Elders <br/>
*  waiting_time_category column was added and categorized as follows:
   0 days -> Same day <br/>
   1 - 7 days -> 1 Week <br/>
   8 - 30 days - > 1 week <br/>
   30 - 60 days -> 1 - 2 months <br/>
   60 - 90 days -> 2 - 3 months <br/>
   90 - 180 days -> 3 -6 months <br/>
   
### Conclusion
* Nearly 20% of the dataset resulted in No shows. It was also observed that although every row in the dataset corresponded to a unique appointment ID, patient IDs were not unique. This means there were patients who have scheduled appointments more than once. This could affect the proportion of no shows in the dataset.
* The factors that are important for us to know if a patient will show up for their scheduled appointment are age group, hipertension, diabetes, alcoholism, waiting time (difference between Scheduled Day and Appointment Day), Scholarship and Handicap.
* The least number of no shows were when appointments were scheduled on the same day. If appointments were scheduled 1 to 2 months from the scheduled day of the appointment, the number of no shows increased. The proportion of no shows increases from Same Day to 1- 2 Months waiting time but then decreases.
* It can be said that patients would show up more on a Weekend i.e. Saturday compared to other weekdays. However, number of appointments scheduled on weekdays is more than on weekends.
* Jardim Camburi is the neighbourhood that has maximum number of no-show appointments. Nothing more could be concluded from the dataset.
* The proportion of female patients who did not show up is very similar to that of their male counterparts. This means gender does not have an impact on patients not showing up for their scheduled appointment.
* As no statistical tests are included in this analysis, these are findings based on exploratory data analysis done on different features.
