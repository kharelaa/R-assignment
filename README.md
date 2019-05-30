# R-assignment
It includes coding for the first part of the assignment, including code used to import csv file.
It includes code that helps calculate the average and standard deviation of tree circumference at the start and end of the study at both sides. Additionally, box plots of tree circumferences are made for the start and end of the study.

Command and description both displayed when viewed under "Raw" format

#Command to read .csv document and save it under 't'
t<-read.csv("https://github.com/markziemann/SLE712_files/raw/master/week10_files/growth_data.csv")

#To display data stored under 't'
t

#Provide summary of information stored under 't'. It includes mean, median, standard deviation as well.
summary(t)

#makes a new heading named 'mean_northeast_1999' and stores the mean value for column 3, rows 1 to 51
mean_northeast_1999<-mean(as.matrix(t[1:51,3]))

#shows the calculated mean value
mean_northeast_1999

#makes a new heading named 'sd_northeast_1999' and stores the standard deviation value for column 3, rows 1 to 51
sd_northeast_1999<-sd(as.matrix(t[1:51,3]))

#shows the calculated standard deviation value
sd_northeast_1999

mean_southwest_1999<-mean(as.matrix(t[52:100,3]))

mean_southwest_1999

sd_southwest_1999<-sd(as.matrix(t[52:100,3]))

sd_southwest_1999

mean_northeast_2019<-mean(as.matrix(t[1:51,6]))

mean_northeast_2019

sd_northeast_2019<-sd(as.matrix(t[1:51,6]))

sd_northeast_2019

mean_southwest_2019<-mean(as.matrix(t[52:100,6]))    

mean_southwest_2019

sd_southwest_2019<-sd(as.matrix(t[52:100,6]))

sd_southwest_2019

#shows boxplot for data stored under circumf_1999_cm for 1 to 51 row number. ylab command renames the y-axis
boxplot(t$Circumf_1999_cm[1:51],ylab="Northeast_Circumf_1999_cm")

boxplot(t$Circumf_2019_cm[1:51],ylab="Northeast_Circumf_2019_cm")

boxplot(t$Circumf_1999_cm[52:100],ylab="Southwest_Circumf_1999_cm")

boxplot(t$Circumf_2019_cm[52:100],ylab="Southwest_Circumf_2019_cm")

summary((t$Circumf_2019_cm[52:100]))

