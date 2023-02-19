# Name: Ashley Allen
# A6: Consumers, Windowing, and Multiple Channels
 Design and Implement a producer for the Smart Smoker App
 
## Before You Begin

1. Fork this starter repo into your GitHub.
1. Clone your repo down to your machine.
1. View / Command Palette - then Python: Select Interpreter
1. Select your conda environment. 

## How to run this program:

Files ton hat needs to be used:

bbq_producer.py

Check your host to ensure you are using "localhost"
Determine if you would like to have the RabbitMQ website prompt you to open.

There are 4 columns in this csv file
Time = Date-time stamp for the sensor reading
Channel1 = Smoker Temp
Channel2 = Food A Temp
Channe3 = Food B Temp
Assignment - Smart Smoker

## Using a Barbeque Smoker

When running a barbeque smoker, we monitor the temperatures of the smoker and the food to ensure everything turns out tasty. Over long cooks, the following events can happen:

The smoker temperature can suddenly decline.

## Sensors

We have temperature sensors track temperatures and record them to generate a history of both (a) the smoker and (b) the food over time. These readings are an example of time-series data, and are considered streaming data or data in motion.

## Streaming Data

Our thermometer records three temperatures every thirty seconds (two readings every minute). The three temperatures are:

the temperature of the smoker itself.
the temperature of the first of two foods, Food A.
the temperature for the second of two foods, Food B.
Significant Events

## We want know if:

The smoker temperature decreases by more than 15 degrees F in 2.5 minutes (smoker alert!) Any food temperature changes less than 1 degree F in 10 minutes 

## Smart System

Python:

Simulate a streaming series of temperature readings from our smart smoker and two foods. Create a producer to send these temperature readings to RabbitMQ. Create three consumer processes, each one monitoring one of the temperature streams. Perform calculations to determine if a significant event has occurred.

##Consumer Requirements
The smoker temperature decreases by more than 15 degrees F in 2.5 minutes (smoker alert!)
Any food temperature changes less than 1 degree F in 10 minutes (food stall!)

## Screenshot of Producer Running:

<img width="809" alt="Terminal" src="https://user-images.githubusercontent.com/95989498/218274091-0c80bac9-f9c6-416a-905b-cee0e25bae4e.png">

## Screenshot of Consumer Running:

<img width="669" alt="Producer:Consumer" src="https://user-images.githubusercontent.com/95989498/219905553-67e65d0b-1a65-4bba-8f7b-0689a617ff93.png">

## Screenshot of Smoker_Alert Running:

<img width="883" alt="Smoker_Alert" src="https://user-images.githubusercontent.com/95989498/219905567-7e192ec0-44c1-4f27-87b0-d653117f18ec.png">

<img width="796" alt="Smoke_Alert 2" src="https://user-images.githubusercontent.com/95989498/219909953-71995ad1-7838-4c76-bf8b-ea2464aa1745.png">

## Screenshot of Food A & B Consumer Running:

<img width="866" alt="Food A   B Consumer" src="https://user-images.githubusercontent.com/95989498/219910136-f4d12449-5e20-4407-a935-d2f5f7995095.png">
