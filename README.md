# Task 1 - (Simple Linear Regression)

# Gettung the data from csv file.

Score = read.csv(file.choose(), header = T)

# To check that we got the data correctly

View(Score)

cor(Score$Hours,Score$Scores)

# We got postive correlation 

task = lm(Scores~Hours, data = Score)

plot(Score$Hours,Score$Scores, main = 'scatter plot')

abline(task, col = "black")

summary(task)

# To get the estimated predicted answer.

ans= data.frame(Hours=9.25)

predict(task,ans)

