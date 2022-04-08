# PStocks

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
1. [Schema](#Schema)

## Overview
### Description
This app takes information from an API and allows users to search for stocks' stats and prices and add stocks into favorites to be displayed separately.

### App Evaluation

- **Category:** Stocks / Finance / Business
- **Mobile:** This app will be development with mobile in mind but could also be implemented for computers and other devices.
- **Story:** Shows stats and history of stocks and allow user to have very current and pass evaluation of specific companies in the market.
- **Market:** Any person interested on investing in stocks and the market can use this app and will allow them to personally use that information as per their own convenience.
- **Habit:** This app could be use anytime depending on how often they want to be informed about the stock market.
- **Scope:** We will have first the most current popular stocks and later as the user add stocks to favorite, they will appear at the top.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories (users should be able to)**

- Search for stocks by name
- See the graph of the stocks by: seconds, minutes, days, years
- Read description of the stock
- A general description of the latest news
- Add favorites stocks

**Optional Nice-to-have Stories**

- Compare stocks prices
- See real time stocks
- Change graphs styles

### 2. Screen Archetypes

- List of favorite stocks with a search bar at the top
- View of selected stock description

### 3. Navigation

**Tab Navigation** (Tab to Screen)

- Favorite stocks
- All stocks ordered by latests highest changes

**Flow Navigation** (Screen to Screen)

- See favorite stocks view -> Search bar for stocks
- Profile -> Go to latests stocks with highest changes

## Wireframes

<img src="https://user-images.githubusercontent.com/45988719/162541605-f1daf102-1d5b-4063-b130-899b94cab8ea.jpeg" width=800><br>

### [BONUS] Digital Wireframes & Mockups

Favorite Stocks             |  Remove Favorite         | All Stocks             |  Stocks Detail View       | Detail View Favorite         
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
<img src="https://user-images.githubusercontent.com/45988719/162543078-b956145d-6584-485f-9808-fb56e059e277.png" width=200><br>  |<img src="https://user-images.githubusercontent.com/45988719/162543130-264d19ff-d43c-4a9f-bddc-7e15052dd23f.png" width=200><br>|<img src="https://user-images.githubusercontent.com/45988719/162543157-2d6a86bd-4f25-4131-b77c-880803be2bab.png" width=200><br>|<img src="https://user-images.githubusercontent.com/45988719/162543176-d9c52f39-fe1e-49ab-a57f-e07679d06d30.png" width=200><br>|<img src="https://user-images.githubusercontent.com/45988719/162543199-76966904-ea5e-4bb6-bd8d-b744901dcef9.png" width=200><br>


## Schema 
### Models
#### Stocks Information Open Market

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | stockId	| String	| unique id that identify each stocks. e.g: GOOG, S&P 500, etc… |
| stockName	| String	| name of the stock |
| stockExchange	| String	| stock exchange the stock belongs to. e.g: Nasdaq |
| stockDescription	| String	| brief description of what the stock is about |
| stockStats	| json	| keep track of the stocks changes, this helps build a graph |
| favoriteAt	| DateTime	| hold the time the stock was added to favorites |
| open	| Number	| price when the  market opened |
| high	| Number	| highest value of the stock |
| low	| Number	| lowest value of the stock |
| vol	| Number	| volume of the stock |
| p_e	| Number	| price/earning ratio |
| mktCap | Number	| market capitalization |
| wH52	| Number	| highest value security has traded |
| wL52	| Number	| lowest value security has traded |
| avgVol	| Number	| average stock volume |
| yield	| Number	| earnings generated over investing (in percentage) |
| beta	| Number	| stock volatility vs the market |
| eps	| Number	| earnings per share |

#### Stocks Information Closed Market
   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
| stockId	| String	| unique id that identify each stocks. e.g: GOOG, S&P 500, etc… |
| stockName	| String	| name of the stock |
| favoriteAt	| DateTime	| hold the time the stock was added to favorites |
| stockExchange	| String	| stock exchange the stock belongs to. e.g: Nasdaq |
| stockDescription	| String	| brief description of what the stock is about |
| stockStats	| json	| keep track of the stocks changes, this helps build a graph |
| clockAt	| Number	| the last price when the market closed |
| afterHours	| Number	| the last price after hours of the closing market |


#### Stocks' News
   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | newsSource	| String	| news Company Description |
| postedAt	| DateTime	| the date the news was release |
| newsDescription	| String	| brief summary of the news related to the stock |
| newsLink	| String	| url redirect to news |

