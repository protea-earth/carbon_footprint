# carbon_footprint
![](https://github.com/protea-earth/carbon_footprint/blob/master/assets/logo.png)

Calculate your carbon footprint easily using a command line interface. 

Built by [Protea](http://protea.earth), the world's leading social network community to reduce your effect on the climate.

## Getting started

First, clone the repository:

```
git clone git@github.com:protea-earth/carbon_footprint.git
```

Now install all the dependencies:

```
pip3 install -r requirements.txt 
```

Now run the script 

```
python3 carbon_footprint.py
```

You can then answer all the questions provided:

```
Jims-MBP:carbon_footprint jimschwoebel$ python3 carbon_footprint.py
pygame 1.9.4
Hello from the pygame community. https://www.pygame.org/contribute.html
please type answers to the following questions below
what is your email? 
jim@protea.earth
How many people are in your household? (e.g. 2) 
2
What is your electric bill (in dollars) monthly?  (e.g. 50) 
50
How many flights do you take per year? (e.g. 10) 
10
Do you own a car? (e.g. n | y) 
n
What is your average distance to commute to/from work in miles - for example 21? (e.g. 10) 
1
Do you use public transportation? (e.g. y)
y
Do you use uber or another ride sharing platform like Lyft? (e.g. y) 
y
How many ride-sharing trips do you complete per month? (e.g. 10) 
10
Are you a vegetarian? (e.g. n) 
n
Do you eat meat more than 3 times each week? (e.g. y) 
y
How much money do you spend on Amazon per month in US dollars - for example, fifty dollars? (e.g. 150) 
150
{'email': 'jim@protea.earth', 'answers': ['2', '50', '10', 'no', '1', 'yes', 'yes', '10', 'no', 'yes', '150'], 'footprint': 7710.966198878506, 'footprintbytype': [1401.8691588785048, 2868.8, 427.25239999999997, 2993.70964, 19.334999999999997], 'footprint_delta': -6949.883801121495, 'footprintbytype_delta': [-5850.890841121495, 2266.3500000000004, -4088.0176000000006, 725.74964, -3.075000000000003], 'labels_footprint': ['electric (kg Co2/year)', 'flight (kg Co2/year)', 'transportation (kg Co2/year)', 'food (kg Co2/year)', 'retail (kg Co2/year)'], 'labels_footprintbytype': 'total kg Co2/year'}
2993.70964
['Electricity consumption (kwh * 1000)', '# of flights per year', '# commute miles per year (thousands)', '# of uber trips per year', 'food choice (tons of CO2 emissions/year)']
[4, 10, 0, 120, 2]
[11, 2, 15, 7, 2]
['electricity', 'flights', 'transportation', 'food', 'retail']
[1401, 2868, 427, 2993, 19]
[7252, 602, 4515, 2267, 22]
['1.pdf', '2.pdf', '3.pdf', '4.pdf', '5.pdf', '6.pdf', '7.pdf', '8.pdf']
```

After this, a [.PDF report](https://github.com/protea-earth/carbon_footprint/blob/master/footprint_report.pdf) will pop up with your results.

## [Reports](https://github.com/protea-earth/carbon_footprint/blob/master/footprint_report.pdf)

Reports look like [this](https://github.com/protea-earth/carbon_footprint/blob/master/footprint_report.pdf), and generate figures like the ones below that highlight your carbon consumption relative to the average American. 

### Carbon consumption by category (by label)
![](https://github.com/protea-earth/carbon_footprint/blob/master/assets/bar.png)
### Carbon consumption by category (kg Co2/year)
![](https://github.com/protea-earth/carbon_footprint/blob/master/assets/bar_2.png)
### Carbon consumption % by category 
![](https://github.com/protea-earth/carbon_footprint/blob/master/assets/pi.png)

## [Assumptions](https://github.com/protea-earth/carbon_footprint/blob/master/assets/7.pdf) in carbon footprint 
### Electricity:
- Electric bill - 11,698 kwh/year = average energy consumption / household.
- the U.S. average is 13.27 cents per kilowatt hour (kwh), 0.62 kilogramCO2 / kwh.
- 11,698 kwh/year * 0.62 kgCO2/kwh = 7,252.76 kg CO2/year.
### Flights per year:
- Flights per year - average is 2.1 trips per American (if fly).
- Assume 0.1304 kgCO2/km for medium-term flights (DEFRA model).
- Domestic flights ~2.5-3 hr, 2200km * 0.1304 kgCO2/km * 2.1 trips = 602.448 kg CO2/yr.
### Transportation:
- Average American drives around 15,000 per year (assume this is all forms of ground transport).
- Fuel efficiency on car - assume 30 mpg on road car now.
- 0.960 pounds = 0.435 kg CO2 per mile (driving) * 15,000 miles/year = 6,525.0 kg CO2 / year. 
- 0.657 pounds = 0.298 kg of CO2 per mile - 50% public transport, 50% single auto * 15,000 miles/year = 4470.0 kg CO2 /year.
- 0.354 pounds = 0.161 kg of CO2 per mile (public transportation) * 15,000 miles / year = 2,415.0 kg CO2 / year.
### Uber trips:
- (14 uber million trips / day * 0.50)9 / 325 million people (USA) * 365 days / year = 7.86 rides/person in the USA (assumes 50% of all uber rides are in the USA).
- Average ride length = 6 miles/trip * 7.86 trips / person / year * 0.960 kgCo2/mile = 45.27 kg Co2/uber rider/year.
### Food choices / nutrition:
- 1.7 US tons = 1,542.21406 kilograms of CO2/year - vegetarian.
- 2.5 US tons = 2,267.96185 kilograms of CO2/year - average.
- 3.3 US tons = 2,993.70964 kilograms of CO2/year - meat lover.
### Amazon supply chain:
- 0.1289 kg CO2e per dollar (USD).
- 3,300,000 boxes/day13 * 365 days/year / 325,000,000 Americans = 3.70 boxes/American.
- 3.70 boxes/year * $47 / box = ~$173.90/year * 0.1289 kg / $1 USD= 22.41 kg CO2/year.

## Getting involved
Here are some ways you can get more involved:

* register an account @ [Protea.Earth](http://start.protea.earth), a social network community designed to reduce your carbon footprint.
* give some feedback on this repository by opening up a [GitHub issue](https://github.com/protea-earth/carbon_footprint/issues).
* send me an email @ jim@protea.earth; I'm always interested to chat about voice computing and/or climate change!

## References
- [Shrinkthatfootprint.com](http://shrinkthatfootprint.com/average-household-electricity-consumption)
- [Chooseenergy.com](https://www.chooseenergy.com/electricity-rates-by-state/)
- [Quora](https://www.quora.com/How-much-CO2-is-produced-per-KWH-of-electricity)
- [Airlines.org](http://airlines.org/wp-content/uploads/2016/04/2016Survey.pdf)
- [Environmental Change Institute](https://www.eci.ox.ac.uk/research/energy/downloads/jardine09-carboninflights.pdf)
- [Reference.com](https://www.reference.com/vehicles/average-mileage-put-car-year-5c8f88fa02be73c8)
- [Wikipedia](https://en.wikipedia.org/wiki/Corporate_average_fuel_economy)
- [Tranistscreen.com](http://blog.transitscreen.com/how-public-transit-can-and-must-help-reduce-carbon-pollution)
- [Businesofapps.com](https://www.businessofapps.com/data/uber-statistics/)
- [Ride.guru](https://ride.guru/lounge/p/what-is-the-average-trip-distance-for-an-uber-or-lyft-ride)
- [Shrinkthatfootprint.com](http://shrinkthatfootprint.com/food-carbon-footprint-diet)
- [AboutAmazon.com](https://sustainability.aboutamazon.com/carbon-footprint)
- [Quora](https://www.quora.com/How-many-boxes-does-Amazon-ship-every-day)
