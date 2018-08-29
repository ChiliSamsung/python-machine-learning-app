League of Legends Game Predictor

Charles Sansone and Hannah Walsh

Here we wanted to explain what exactly our code does/did so we could create our project. 
As you probably already know, our project was to scrape Riot Games's API and create a model that, 
when given two teams of five players, will predict which team will win. We will divide our 
project into three parts: 1) getting the data, 2) making the model, and 3) having the model predict when given the right input. 

PART 1: Getting the data

We left all the code that we used to scrape Riot's API in even though it doesn't actually do anything in our main function. 
We created various different functions to obtain and parse data about different players. We had other functions that 
combined that data into a statistics per team, and then we went and found out, when these teams played each other 
in the past, which team won. All this was done using responses and parsing. Finally, we had a function called 
make_dataset that took in a list of match IDs and outputted a list of our desired statistics. Everything before 
make_dataset was used to scrape and obtain the data that you see in the train txt file. 

PART 2: Making the model

Next came creating the model. We created a Logistic Regression model but to do that, we had to parse our 
list of dictionaries into a csv file, which we did right after our data scraping code. Once we parsed our 
list of statistics into a csv file, we plugged it into the model. Then we used RDE to find out which of the 
14 statistics that we obatined from each time were the most important. After doing that, we remade that model 
and made it consider those statistics much more heavily in its predictions.

PART 3: Predicting given input

Our function called predict_game takes in 10 summoner names (they are basically League of Legends usernames), 
where the first 5 are part of the blue team and the last five are part of the red team. It then gets the 
statistcal data on those people and puts it into a csv file and then we feed that file into the model and 
ask it to predict the outcome. It will print whether or not the red or blue team wins to the console!

This is how our project works, we wanted to leave all the code in so you could see all the progress 
we made and how we obtained the data that we used. Thanks so much for such a great class!
