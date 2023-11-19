# Week4_Ana505
Ibai Vidaurreta
Wekk 4 R Assignment

#Task: Write the function to get a dataset from Base R: Titanic
> library(datasets)
> data(Titanic)
> Week4 <- as.data.frame(Titanic)

#TASK: Write the function to see the top rows of the data
> as_tibble(Week4)
>
#TASK: Write the functions to install and call dplyr
> install.packages("dplyr")
>library(dplyr)
> 
#Task: Write the function to 'select' the Survived and Sex columns
> Columns <-select(Week4, Survived, Sex)
> print(Columns)
>
> #TASK: Write the function to save the two columns as one new dataset
> survived_sex_dataset <-select(Week4, Survived, Sex)
>
> #TASK: Write the function that deselects the sex column
> survived_dataset <-select(survived_sex_dataset, -Sex)
>
> #TASK: Write the function that renames 'Sex' to 'Gender'
> rename(Week4, Gender = Sex)
>
> #TASK: Write the function that names a new dataset that includes the 'gender' column
> Gender_dataframe <- rename(Week4, Gender=Sex)
>
> #TASK: Write the function that includes only rows that are 'male'
> Male <-filter(Gender_dataframe, Gender == "Male")
>
> #TASK: Write the function to group the data by gender (hint: arrange())
> Arranged <- arrange(Gender_dataframe, Gender)
>
> #TASK: Sum the Freq column
>#TASK: After you run it, write the total here:2201
sumFreq <-sum(Week4$Freq)
>
> #TASK: Write the function that includes only rows that are 'female'
> Female <-filter(Gender_dataframe, Gender == Female)
>
> #TASK: Write the function that joins the male and female rows
> Both_Gender <- union(Male, Female)
>
> #Optional Task: add any of the other functions
> Relocate_Columns <- relocate(Week4, Survived, Before = Sex)



