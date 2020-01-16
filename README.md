# Project Overview
The Starbucks project was my capstone project for the Udacity Data Scientist Nanodegree. This data was provided by Starbucks to simulate their customers and transactions to see if there are better approaches to sending customers specific promotional deals. 

# Introduction
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

Your task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.

You'll be given transactional data showing user purchases made on the app including the timestamp of purchase and the amount of money spent on a purchase. This transactional data also has a record for each offer that a user receives as well as a record for when a user actually views the offer. There are also records for when a user completes an offer.

Keep in mind as well that someone using the app might make a purchase through the app without having received an offer or seen an offer.


# File Description
Here is a quick overview of data files provided:
1. Profile - Dimensional data about each person, including their age, salary, and gender. There is one unique customer for each record.
2. Portfolio - Information about the promotional offers that are possible to receive, and basic information about each one including the promotional type, duration of promotion, reward, and how the promotion was distributed to customers
3. Transcript - Records show the different steps of promotional offers that a customer received. The different values of receiving a promotion are receiving, viewing, and completing. You also see the different transactions that a person made in the time since he became a customer. With all records, you see the day that they intereacted with Starbucks and the amount that it is worth.

# Profile Portfolio and Transcript Data.zip
Three JSON files that show profiles of customers, promotional deals that are offered, and the transaction history of customers.

portfolio.json

- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

profile.json

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

transcript.json

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record


Acknowledgements
Many thanks to [udacity](www.udacity.com) for offering great [Data SCientist Nanodegree course](https://www.udacity.com/course/data-scientist-nanodegree--nd025)
I also wish to thank [starbucks](https://www.starbucks.com/) for providing the datasets.



