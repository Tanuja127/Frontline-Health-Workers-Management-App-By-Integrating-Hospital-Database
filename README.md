# Frontline-health-workers-management-app-by-integrating-hospital-database

This code contains the basic design of our idea ,where patient details will be given as input and would be stored in csv file. A unique barcode will be generated for each patient, by scanning which the patient data will be displayed. We also have provision for updating the patient’s data periodically. The other part of the code is to send the notification to the nurses periodically. 

# Hardware 

•	Arduino Uno

•	Mini barcode scan engine

•	Display

•	 TP4056 1A Li-Ion Battery Charging Board Micro USB with Current Protection

•	 Lithium ion battery chargable

# Software
•	 Python 3

•	 Arduino 2.0

•	 DB Browser for SQLITE3

# Process flow

1. The patient data is entered into the main database and gets stored in it as csv file
2. Unique barcode is generated which also gets stored in csv file, which can be printed.
3. The patient data , medications can be updated .
4. Notification for each patient will be triggered by the database .
5. Other timely notification for the nurses will also be received.
6. As the code was getting comlex and the time given to us was not sufficient, the full system code is yet to be done,and also cloud integration is pending.

# Data flow digram

  ![image](https://user-images.githubusercontent.com/80504455/119348810-fc6ef080-bcba-11eb-8bc7-31c150afd8aa.png)
  
#  Working Structure:
     
# 1.Appointment
1) Using DB Browser for SQLITE3, create a database containing the columns ID, Name, Age, Gender, Location, Phone, Appointment_Date
2) We add the database file to the python IDE.
3) Create frames where we enter the details of the patient and we add appointment which is automatically stored in the database created earlier.
                    
# 2.Update
1) This is where we update the details of the patients when any changes are to be made. It is a simple module where we enter the name of the patient and the              required changes can be made.These updated detail is stored automatically to the database.
2) We import the database file to csv and the barcode is generated using the Barcode Format.
   
# 3.GENERATING NOTIFICATIONS
1)	Using pandas, we are reading the csv file and importing datetime library.
2) We are arranging the dataset in ascending order with respect to time, to make it convenient to generate notifications in an orderly manner. 
3) We have grouped the dataset based on the time of dosage, in order to not miss any patients. Just in case, two patients are to be given dosage at the same                 time notification would be sent at the same time to the nurse.
4)	From win10toast library, we have imported ToastNotifier module to generate notifications.
5) We are reading through each time instance in the dataset and comparing it with the present time, if it matches it generates a notification.
6) Nurses’ health is important as well, so we designed a notification system to remind them of their meal breaks and a gratitude message at the end of their                         shift.         
   
                     
                   
                   
                   
                   
                   
                   
 
# Contributed By

TANUJA D

SWETHA S

SUBHIKSHA M

SAI LIKHITHA P

