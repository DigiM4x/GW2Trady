GW2Trady
========


GW2Trady - An application of machine learning to Guild Wars 2 TP data.


PURPOSE:
The primary purpose of this project is to apply a wide variety of machine learning techniques to the Guild Wars 2 Trading Post data in an attempt to create an 'advice bot' which can recomend the investments most likely to be profitable at any given time. The various algorithms will then be compaired and contrasted with an analysis of their varied effectiveness at this task.


CREDIT WHERE DUE:

I would like to thank Ruben de Vries and the rest of the gang working on gw2spidy.

https://github.com/rubensayshi/gw2spidy

http://www.gw2spidy.com/

This is a stand alone project, implimented with different languages and independantly of Ruben's work, but was inspired by his wonderful website. Ruben was also kind enough to provide me with training data for this project from his own personal database. I hope to work closely with him in the future, and the name of this project is in small tribute to the spider that spawned it.


PLAN:

1) Obtain data.
- Migrate the data from MySQL to MSSQL.

2) Explore data with traditional human exploration.

3) Embelish the data.
- Add measured metrics which could be useful such as spread, daily average, average daily variance, etc.
- Make space for computed values, such as the estimated probability of 24 hour resale at current prices.
- Add anything else which might seem like a good idea. Most of this will come out during step 2.

4) Create a Machine Learning Shell (MLS)
- Create a shell program which will accept any encapsulated machine learning algorithm and dataset.
- Create base classes for each component of the shell.
- Create one simple implimentation of each component of the application.
- Test, refine, and improve.

5) Use the first round implimentation of the MLS to approximate values which were left blank in step 3.ii.

6) Using the MLS, create a single continuous value which represents the 'value' of an investment.
- The details of this step will be determined later.

7) Create a testing shell.
- This shell will accept the output of the MLS as an implimentation of a base 'algorithm' class.
- It will accept logic to calculate the actual value as an implimentation of a base 'target' class.
- It will use the provided algorithm to determine the predicted values and compare them to the actual values.
- It will return the results in a meaningful way, so that the results of different machine learning algorithms can be quickly evaluated.

7) Create an artificial trader.

- This will use the investment value index to simulate making purchases and reselling on the trading post.
- This test shell will have a generic overridable component which determines investment strategy based on that information, so that different investment strategies can be quickly tested for efficacy. 
- This testing shell will keep track of profits made, and will be able to show total profits over short and long term goals for evaluation of different stategies.
- This MAY eventually apply more advance AI training technologies and/or apply genetic algorithms to the trading strategy to create a more robust pro-trader system.

8) Iterate

- Create additional implimentations of machine learning algorithms for use in the MLS.
- Train and test these implimentations.
- Compare and contrast.


This project will be implimented in MSSQL and python.



CURRENT STATUS: Shelved due to life circumstances.
