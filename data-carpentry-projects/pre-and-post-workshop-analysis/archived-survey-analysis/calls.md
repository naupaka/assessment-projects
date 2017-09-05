

```r
#! /usr/bin/env Rscript

#
#   Description: report plotting calls
#   Analyzing pre and post survey results from Data Carpentry 
#   Repo: https://github.com/carpentries/assessment-projects/tree/master/data-carpentry-projects
#   Date: 2017, August 27
#   Copyright (C) 2017 Paula Andrea Martinez
#   ORCID iD 0000-0002-8990-1985

source(file = "scripts/exploringData.R")
```

```
## Warning in file(filename, "r", encoding = encoding): cannot open file
## 'scripts/exploringData.R': No such file or directory
```

```
## Error in file(filename, "r", encoding = encoding): cannot open the connection
```

```r
# ###########################################################################
# Calls 
# Run line by line
# ###########################################################################
```

```r
Epreworkshop <- Exploring("data/preworkshop_public_archived.csv")
```

```
## Error in Exploring("data/preworkshop_public_archived.csv"): could not find function "Exploring"
```

```r
Epreworkshop <- cleanPreworkshopdata(Epreworkshop)
```

```
## Error in cleanPreworkshopdata(Epreworkshop): could not find function "cleanPreworkshopdata"
```

```r
plotByStatusGeneric(Epreworkshop, "Pre-survey", "year.survey" , "year of survey response")
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "year.survey", : could not find function "plotByStatusGeneric"
```

```r
plotByStatusGeneric(Epreworkshop, "Pre-survey", "First.Time" , "first time taking a DC as learner", c(2,1))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "First.Time", : could not find function "plotByStatusGeneric"
```

```r
# Simple barplot for discipline, Biology has the majority of answers
plotBarplot(Epreworkshop, "Pre-survey", "Discipline", "discipline")
```

```
## Error in plotBarplot(Epreworkshop, "Pre-survey", "Discipline", "discipline"): could not find function "plotBarplot"
```

```r
plotByStatusGeneric(Epreworkshop, "Pre-survey", "OS" , "operative system", c(1,2,4,3))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "OS", "operative system", : could not find function "plotByStatusGeneric"
```

```r
# table(Epreworkshop$With.Friend)
plotByStatusGeneric(Epreworkshop, "Pre-survey", "With.Friend" , "attended with a friend", c(3,1,2))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "With.Friend", : could not find function "plotByStatusGeneric"
```

```r
# table(Epreworkshop$Programming.Usage)
plotByStatusGeneric(Epreworkshop, "Pre-survey", "Programming.Usage" , "programming usage", c(2, 3, 6, 4, 7, 1, 5))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "Programming.Usage", : could not find function "plotByStatusGeneric"
```

```r
# Skipping current tools "Current.Tools.1" to "Current.Tools.7"
# table(Epreworkshop$Have.Dataset)
plotByStatusGeneric(Epreworkshop, "Pre-survey", "Have.Dataset" , "having a dataset", c(2,1,4,3))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "Have.Dataset", : could not find function "plotByStatusGeneric"
```

```r
# "Data.Management.Strategy" "Data.Analysis.Workflow" are better plotted with a Likert plot 
# table(Epreworkshop$Data.Management.Strategy)
# table(Epreworkshop$Data.Analysis.Workflow)
plotByStatusGeneric(Epreworkshop, "Pre-survey", "Data.Organization" , "importance of data organization", c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "Data.Organization", : could not find function "plotByStatusGeneric"
```

```r
# table(Epreworkshop$Using.Scripting.Language)
plotByStatusGeneric(Epreworkshop, "Pre-survey", "Using.Scripting.Language" , "importance of using a scripting language",  c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "Using.Scripting.Language", : could not find function "plotByStatusGeneric"
```

```r
# ### Skipped because question is not clear
# table(Epreworkshop$Using.R.or.Python)
# table(Epreworkshop$Value.of.SQL.or.Python)
# Taken in the US
# table(Epreworkshop$Workshop.in.US)
# 31% No 69% Yes
#(590 * 100) / 1890  
# ### [1] 31.21693
#(1307 * 100) / 1890  
# ###[1] 69.15344
plotByStatusGeneric(Epreworkshop, "Pre-survey", "Workshop.in.US" , "workshop taken in the US")
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "Workshop.in.US", : could not find function "plotByStatusGeneric"
```

```r
# make workshop in the US per year
plotGeneric(Epreworkshop, "Pre-survey", "Workshop.in.US" , "workshop taken in the US per year", c(2,1), "year.survey" )
```

```
## Error in plotGeneric(Epreworkshop, "Pre-survey", "Workshop.in.US", "workshop taken in the US per year", : could not find function "plotGeneric"
```

```r
# this is very interesting, shows that for 2017 only 10% of respondents have taken the survey outside of the US
plotByStatusGeneric(Epreworkshop, "Pre-survey", "Age" , "age")
```

```
## Error in plotByStatusGeneric(Epreworkshop, "Pre-survey", "Age", "age"): could not find function "plotByStatusGeneric"
```

```r
plotGeneric(Epreworkshop, "Pre-survey", "Age" , "age per year",NULL, "year.survey")
```

```
## Error in plotGeneric(Epreworkshop, "Pre-survey", "Age", "age per year", : could not find function "plotGeneric"
```

```r
# doesn't really mean that more people in the US came with a friend, it just looks like that because more people
# have taken the survey in the US
plotGeneric(Epreworkshop, "Pre-survey","With.Friend" , "came with friend vs taken in the US", c(3,1,2), 
            "Workshop.in.US" , c(2,1)) 
```

```
## Error in plotGeneric(Epreworkshop, "Pre-survey", "With.Friend", "came with friend vs taken in the US", : could not find function "plotGeneric"
```

```r
plotGeneric(Epreworkshop, "Pre-survey", "OS", "OS vs taken in the US", c(1,2,4,3), "Workshop.in.US" , c(2,1)) 
```

```
## Error in plotGeneric(Epreworkshop, "Pre-survey", "OS", "OS vs taken in the US", : could not find function "plotGeneric"
```

```r
plotGeneric(Epreworkshop, "Pre-survey", "OS", "OS vs year of the survey", c(1,2,4,3), "year.survey" ) 
```

```
## Error in plotGeneric(Epreworkshop, "Pre-survey", "OS", "OS vs year of the survey", : could not find function "plotGeneric"
```

```r
# Filter all of those who did not take the survey in the US 
EpreworkshopUS <- subset(Epreworkshop, Workshop.in.US == "Yes")
```

```
## Error in subset(Epreworkshop, Workshop.in.US == "Yes"): object 'Epreworkshop' not found
```

```r
dim(EpreworkshopUS)
```

```
## Error in eval(expr, envir, enclos): object 'EpreworkshopUS' not found
```

```r
plotByStatusGeneric(EpreworkshopUS, "Pre-surveyUS", "Age" , "age")
```

```
## Error in plotByStatusGeneric(EpreworkshopUS, "Pre-surveyUS", "Age", "age"): could not find function "plotByStatusGeneric"
```

```r
# Gender... this is not a reality, it only means that more women responded in the survey
# not that there were more women have taken the workshop
plotByStatusGeneric(EpreworkshopUS, "Pre-surveyUS", "Gender" , "gender")
```

```
## Error in plotByStatusGeneric(EpreworkshopUS, "Pre-surveyUS", "Gender", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
plotGeneric(EpreworkshopUS, "Pre-surveyUS","With.Friend" , "came with friend vs gender", c(3,1,2), 
            "Gender" ) 
```

```
## Error in plotGeneric(EpreworkshopUS, "Pre-surveyUS", "With.Friend", "came with friend vs gender", : could not find function "plotGeneric"
```

```r
# Names are too long to be shown in categories 
plotByStatusGeneric(EpreworkshopUS, "Pre-surveyUS", "Race" , "race")
```

```
## Error in plotByStatusGeneric(EpreworkshopUS, "Pre-surveyUS", "Race", "race"): could not find function "plotByStatusGeneric"
```

```r
# wordclouds
myWordCloud(Epreworkshop$Department, "Pre-survey_Department")
```

```
## Error in myWordCloud(Epreworkshop$Department, "Pre-survey_Department"): could not find function "myWordCloud"
```

```r
myWordCloud(Epreworkshop$Hope.to.Learn, "Pre-survey_HopeToLearn")
```

```
## Error in myWordCloud(Epreworkshop$Hope.to.Learn, "Pre-survey_HopeToLearn"): could not find function "myWordCloud"
```

```r
# ############################################################################
```

```r
Epostworkshop <- Exploring("data/postworkshop_public_archived.csv")
```

```
## Error in Exploring("data/postworkshop_public_archived.csv"): could not find function "Exploring"
```

```r
Epostworkshop <- cleanPostworkshopdata(Epostworkshop)
```

```
## Error in cleanPostworkshopdata(Epostworkshop): could not find function "cleanPostworkshopdata"
```

```r
# Postworkshop has about half the entries in comparison with the preworkshop 
```

```r
# 2017 has of course less entries because it contains only answers of half a year
plotByStatusGeneric(Epostworkshop, "Post-survey", "year.survey" , "year of survey response")
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "year.survey", : could not find function "plotByStatusGeneric"
```

```r
# there is not much to do with columns that are repeated with the pre-survey
# #  "When.Taking.Survey"        "First.Time"
# # "Research" is a text field wich is difficult to categorize
# table(Epostworkshop$Involvement)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Involvement" , "level of involvement", c(3,1,2))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Involvement", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Practical.Knowledge)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Practical.Knowledge" , "practical knowledge gained", c(1, 3, 2))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Practical.Knowledge", : could not find function "plotByStatusGeneric"
```

```r
plotGeneric(Epostworkshop, "Post-survey", "Practical.Knowledge" , 
            "practical knowledge gained vs level of involvement", c(1, 3, 2),"Involvement", c(3,1,2)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Practical.Knowledge", : could not find function "plotGeneric"
```

```r
# #####The folowwing will be better with a Likert plot
# # "Organize.Data"             "Use.OpenRefine"            "Import.Python"            
# # [13] "Import.R"                  "Visualizations.in.Python"  "Visualizations.in.R"       "Construct.SQL"            
# # [17] "Use.command.line" 
# # For information of each question
# table(Epostworkshop$Organize.Data)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Organize.Data" , "better understanding on how to organize data in spreadsheets", c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Organize.Data", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Use.OpenRefine)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Use.OpenRefine" , "better understanding on how to use OpenRefine for data cleaning", c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Use.OpenRefine", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Import.Python)
# it seems like half of the workshops did not cover python 
plotByStatusGeneric(Epostworkshop, "Post-survey", "Import.Python" , "better understanding on how to import a file in Python and work with the data",  c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Import.Python", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Visualizations.in.Python)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Visualizations.in.Python" , "better understanding on how to do visualizations in Python",  c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Visualizations.in.Python", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Import.R)
# It seems like almost half (40%) of the workshops covered R
plotByStatusGeneric(Epostworkshop, "Post-survey", "Import.R" , "better understanding on how to import a file in R and work with the data",  c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Import.R", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Visualizations.in.R)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Visualizations.in.R" , "better understanding on how to do visualizations in R",  c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Visualizations.in.R", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Construct.SQL)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Construct.SQL" , "better understanding on how to construct SQL queries",  c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Construct.SQL", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Use.command.line)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Use.command.line" , "better understanding on how to use command line",  c(5,1,4,2,6,3)) 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Use.command.line", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Skill.Level.Prior)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Skill.Level.Prior" , "data management and analysis skills prior the workshop", c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Skill.Level.Prior", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
plotGeneric(Epostworkshop, "Post-survey", "Skill.Level.Prior" , 
            "skills prior the workshop vs level of involvement", c(4,1,3,2,5),"Involvement", c(3,1,2)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Skill.Level.Prior", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Skill.Level.Following)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Skill.Level.Following" , "data management and analysis skills following the workshop", c(3,2,4,1))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Skill.Level.Following", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
plotGeneric(Epostworkshop, "Post-survey", "Skill.Level.Following" , 
            "skills level following the workshop vs level of involvement",  c(3,2,4,1),"Involvement", c(3,1,2)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Skill.Level.Following", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Application)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Application" , "can immediately applied what was learned at the workshop", c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Application", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
plotGeneric(Epostworkshop, "Post-survey", "Application" , 
            "can immediately applied what was learned vs level of involvement",  c(4,1,3,2,5),"Involvement", c(3,1,2)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Application", "can immediately applied what was learned vs level of involvement", : could not find function "plotGeneric"
```

```r
# needs to be a big squared plot
plotGeneric(Epostworkshop, "Post-survey", "Application" , 
            "can immediately applied what was learned vs skill level prior the workshop",  c(4,1,3,2,5),"Skill.Level.Prior", c(4,1,3,2,5)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Application", "can immediately applied what was learned vs skill level prior the workshop", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Worth.My.Time)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Worth.My.Time" , "the workshop was worth my time", c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Worth.My.Time", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
plotGeneric(Epostworkshop, "Post-survey", "Worth.My.Time" , 
            "the workshop was worth my time vs level of involvement",  c(4,1,3,2,5),"Involvement", c(3,1,2)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Worth.My.Time", "the workshop was worth my time vs level of involvement", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Material)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Material" , "the material matched the workshop description", c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Material", : could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Recommend)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Recommend" , "would recommend the workshop", c(4,1,3,2,5))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Recommend", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot # big square plot
# great relationship
plotGeneric(Epostworkshop, "Post-survey", "Worth.My.Time" , 
            "the workshop was worth my time vs I will recommend this workshop",  c(4,1,3,2,5),"Recommend", c(4,1,3,2,5))
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Worth.My.Time", "the workshop was worth my time vs I will recommend this workshop", : could not find function "plotGeneric"
```

```r
# Combined plot
plotGeneric(Epostworkshop, "Post-survey", "Recommend" , 
            "I will recommend this workshop vs level of involvement",  c(4,1,3,2,5),"Involvement", c(3,1,2)) 
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Recommend", "I will recommend this workshop vs level of involvement", : could not find function "plotGeneric"
```

```r
# Combined plot
plotGeneric(Epostworkshop, "Post-survey", "Recommend" , 
            "I will recommend this workshop vs it was worth my time",  c(4,1,3,2,5),"Worth.My.Time", c(4,1,3,2,5))
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Recommend", "I will recommend this workshop vs it was worth my time", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Instructors.Effective)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Instructors.Effective" , "were the instructors effective in teaching the workshop?", c(1,2,5,4,3))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Instructors.Effective", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
# great relationship
plotGeneric(Epostworkshop, "Post-survey", "Instructors.Effective" , 
            "were the instructors effective in teaching vs I will recommend this workshop",  c(1,2,5,4,3),"Recommend", c(4,1,3,2,5))
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Instructors.Effective", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Instructors.Enthusiastic)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Instructors.Enthusiastic" , "were the instructors enthusiastic about the workshop?", c(1,2,4,3))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Instructors.Enthusiastic", : could not find function "plotByStatusGeneric"
```

```r
# Combined plot
# great relationship
plotGeneric(Epostworkshop, "Post-survey", "Instructors.Effective" , 
            "instructors were effective in teaching vs instructors were enthusiastic",  c(1,2,5,4,3),"Instructors.Enthusiastic", c(1,2,4,3))
```

```
## Error in plotGeneric(Epostworkshop, "Post-survey", "Instructors.Effective", : could not find function "plotGeneric"
```

```r
# table(Epostworkshop$Workshop.in.US) 
plotByStatusGeneric(Epostworkshop, "Post-survey", "Workshop.in.US" , "the workshop was in the US", c(2,1))
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Workshop.in.US", : could not find function "plotByStatusGeneric"
```

```r
# # age and gender are not shown in the PDF questionnaire
# # not very necesary as given in the presurvey
# table(Epostworkshop$Age)
plotByStatusGeneric(Epostworkshop, "Post-survey", "Age" , "age") 
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Age", "age"): could not find function "plotByStatusGeneric"
```

```r
# table(Epostworkshop$Race.White) # given that is the majority
plotByStatusGeneric(Epostworkshop, "Post-survey", "Race.White" , "white")
```

```
## Error in plotByStatusGeneric(Epostworkshop, "Post-survey", "Race.White", : could not find function "plotByStatusGeneric"
```

```r
# Filter all of those who did not take the survey in the US 
EpostworkshopUS <- subset(Epostworkshop, Workshop.in.US == "Yes")
```

```
## Error in subset(Epostworkshop, Workshop.in.US == "Yes"): object 'Epostworkshop' not found
```

```r
EpostworkshopUS <- droplevels(EpostworkshopUS)
```

```
## Error in droplevels(EpostworkshopUS): object 'EpostworkshopUS' not found
```

```r
# table(EpostworkshopUS$Workshop.in.US)
# table(EpostworkshopUS$Gender)
plotByStatusGeneric(EpostworkshopUS, "Post-survey", "Gender" , "gender")
```

```
## Error in plotByStatusGeneric(EpostworkshopUS, "Post-survey", "Gender", : could not find function "plotByStatusGeneric"
```

```r
# wordclouds
myWordCloud(Epostworkshop$Research, "Post-survey_Research")
```

```
## Error in myWordCloud(Epostworkshop$Research, "Post-survey_Research"): could not find function "myWordCloud"
```

```r
# ############################################################################
```

```r
# not very interesting
multiplot(plotByGender(EpreworkshopUS, "Pre- survey"),
          plotByGender(EpostworkshopUS, "Post- survey"), cols=2)
```

```
## Error in multiplot(plotByGender(EpreworkshopUS, "Pre- survey"), plotByGender(EpostworkshopUS, : could not find function "multiplot"
```

```r
# Gender and status only US surveys
plotByGenderStatus(EpreworkshopUS, "Pre-survey")
```

```
## Error in plotByGenderStatus(EpreworkshopUS, "Pre-survey"): could not find function "plotByGenderStatus"
```

```r
plotByGenderStatus(EpostworkshopUS, "Post-survey")
```

```
## Error in plotByGenderStatus(EpostworkshopUS, "Post-survey"): could not find function "plotByGenderStatus"
```

```r
# filter not answered
newpreGS <- ExcludeNANotGiven(Epreworkshop)
```

```
## Error in ExcludeNANotGiven(Epreworkshop): could not find function "ExcludeNANotGiven"
```

```r
newpostGS <- ExcludeNANotGiven(Epostworkshop)
```

```
## Error in ExcludeNANotGiven(Epostworkshop): could not find function "ExcludeNANotGiven"
```

```r
plotByGenderStatus(newpreGS, "Pre-survey-filtered")
```

```
## Error in plotByGenderStatus(newpreGS, "Pre-survey-filtered"): could not find function "plotByGenderStatus"
```

```r
plotByGenderStatus(newpostGS, "Post-survey-filtered")
```

```
## Error in plotByGenderStatus(newpostGS, "Post-survey-filtered"): could not find function "plotByGenderStatus"
```

```r
# Multiplot
multiplot(plotByGender(newpreGS, "Pre-survey"),
          plotByGender(newpostGS, "Post-survey"), cols=2)
```

```
## Error in multiplot(plotByGender(newpreGS, "Pre-survey"), plotByGender(newpostGS, : could not find function "multiplot"
```

