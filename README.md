# EXP-6-Series-Queues-with-infinite-capacity---Open-Jackson-Network
Date: 19/08/2026


Name : RAM PRASATH S

REG NO : 212224040266

## Aim:
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival of materials follow Poisson process with the mean interval time 12 seconds, service time of lathe machine in series follow exponential distribution with service time 1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.
## Software required:
Visual components and Python

## Theory:

<img width="750" height="401" alt="image" src="https://github.com/user-attachments/assets/0f37f7f6-cd0c-4a76-bbbf-a731f5719366" />

 
## Procedure:
<img width="891" height="208" alt="image" src="https://github.com/user-attachments/assets/54007451-460e-4bb7-a70c-2df3675b27bf" />

 
## PROGRAM:
```
  
  arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
  ser_time1=float(input("Enter the mean inter service time of Lathe Machine 1 (in secs) :  "))
  ser_time2=float(input("Enter the mean inter service time of Lathe Machine 2 (in secs) :  "))
  ser_time3=float(input("Enter the mean inter service time of Lathe Machine 3 (in secs) :  ")
  Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
  lam=1/arr_time
  mu1=1/(ser_time1+Robot_time)
  mu2=1/(ser_time2+Robot_time)
  mu3=1/(ser_time3+Robot_time)
  print("-----------------------------------------------------------------------")
  print("Series Queues with infinite capacity- Open Jackson Network")
  print("-----------------------------------------------------------------------")
  if (lam <  mu1) and (lam <  mu2) and (lam <  mu3):
      Ls1=lam/(mu1-lam)
      Ls2=lam/(mu2-lam)
      Ls3=lam/(mu3-lam)
      Ls=Ls1+Ls2+Ls3
      Lq1=Ls1-lam/mu1
      Lq2=Ls2-lam/mu2
      Lq3=Ls3-lam/mu3
      Wq1=Lq1/lam
      Wq2=Lq2/lam
      Wq3=Lq3/lam
      Ws=Ls/(3*lam)
      print("Average number of objects in the system S1 : %0.2f "%Ls1)
      print("Average number of objects in the system S2 : %0.2f "%Ls2)
      print("Average number of objects in the system S3 : %0.2f "%Ls3)
      print("Average number of objects in the overall system    : %0.2f "%Ls)
      print("Average number of objects in the conveyor S1  :  %0.2f "%Lq1)
      print("Average number of objects in the conveyor S2  :  %0.2f "%Lq2)
      print("Average number of objects in the conveyor S3  :  %0.2f "%Lq3)
      print("Average waiting time of an object in the conveyor S1 : %0.2f secs"%Wq1)
      print("Average waiting time of an object in the conveyor S2 : %0.2f secs"%Wq2)
      print("Average waiting time of an object in the conveyor S3 : %0.2f secs"%Wq3)
  else:
      print("Warning! Objects Over flow will happen in the conveyor")
  print("----------------------------------------------------------------------")
```
## OUTPUT:
 <img width="940" height="458" alt="image" src="https://github.com/user-attachments/assets/2ca05aa3-99de-4c07-bdbc-8c93fa3ff9d9" />


Result
The average number of material in the system and in the conveyor and waiting time are successfully found.
