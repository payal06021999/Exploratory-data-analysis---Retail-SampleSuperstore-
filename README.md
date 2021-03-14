# Exploratory-data-analysis---Retail-SampleSuperstore-
Task 3: Exploratory Data Analysis - As Data Science and Business Analytics Intern at The Sparks Foundation

#The Sparks Foundation
#GRIP March 2021
#Payal Sharma
#Data Science and Business Analytics Intern
#Task 3: Exploratory Data Analysis (Retail)
#Level: Beginner



superstore<-read.csv("C:/Users/HP/Downloads/SampleSuperstore.csv")

names(superstore)
str(superstore)
colSums(is.na(superstore))
summary(superstore)

sum(superstore$Sales)
sum(superstore$Quantity)
sum(superstore$Profit)

library(ggplot2)

table(superstore$Ship.Mode)
ggplot(data=superstore, aes(x=Ship.Mode, fill=Ship.Mode))+geom_bar(width=0.5)

table(superstore$Segment)
ggplot(data=superstore, aes(x=Segment, fill=Segment))+geom_bar(width=0.5)

table(superstore$Region)
ggplot(data=superstore, aes(x=Region, fill=Region))+geom_bar(width=0.5)

table(superstore$Category)
ggplot(data=superstore, aes(x=Category, fill=Category))+geom_bar(width=0.5)

table(superstore$Sub.Category, superstore$Category)
ggplot(data=superstore, aes(x=Sub.Category, fill=Sub.Category))+geom_bar()+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))

ggplot(data=superstore, aes(x=State))+geom_bar()+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))ggplot(data=superstore, aes(x=Quantity))+geom_bar()

ggplot(data=superstore, aes(x=Segment, y=Sales, fill=Segment))+geom_bar(stat="identity",width=0.5)

superstore1<-superstore[superstore$Profit>0,]

ggplot(data=superstore1, aes(x=Segment, y=Profit, fill=Segment))+geom_bar(stat="identity",width=0.5)

ggplot(data=superstore, aes(x=Region, y=Sales, fill=Region))+geom_bar(stat="identity",width=0.5)

ggplot(data=superstore1, aes(x=Region, y=Profit, fill=Region))+geom_bar(stat="identity",width=0.5)

ggplot(data=superstore, aes(x=Category, y=Sales, fill=Category))+geom_bar(stat="identity",width=0.5)

ggplot(data=superstore, aes(x=Sub.Category, y=Sales, fill=Sub.Category))+geom_bar(stat="identity")+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))

ggplot(data=superstore1, aes(x=Category, y=Profit, fill=Category))+geom_bar(stat="identity",width=0.5)

ggplot(data=superstore1, aes(x=Sub.Category, y=Profit, fill=Sub.Category))+geom_bar(stat="identity")+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))

ggplot(data=superstore, aes(x=Category, y=Discount, fill=Category))+geom_bar(stat="identity",width=0.5)

ggplot(data=superstore, aes(x=Sub.Category, y=Discount, fill=Sub.Category))+geom_bar(stat="identity")+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))

ggplot(data=superstore, aes(x=State, y=Sales))+geom_bar(stat="identity", width=0.5)+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))

ggplot(data=superstore1, aes(x=State, y=Profit))+geom_bar(stat="identity", width=0.5)+theme(axis.text.x=element_text(angle=90,hjust=1,vjust=1))






















