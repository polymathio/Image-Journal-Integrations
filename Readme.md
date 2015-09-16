#Image Journal Integrations

The primary (chronologically first) goal of this project is to create integrations between the Fulco API and Salesforce for Nonprofits API (including Causeview fields)

We recommend creating a very small web application which will listen for events from the Fulco API, intake and format the data, and make the appropriate API requests of the Salesforce API. We think that creating this middleware API is the best solution for a few reasons.

1. We have heard from Stuart that there will potentially be many more services and data sources which need to be integrated with Salesforce. We want to write an extensible system that can accept data from multiple sources with a relatively small amount of code refactoring.

2. We want to have the ability to do Test Driven Development to ensure that we are recieving and sending the correct data schema. 

3. We want to store input data be able to control the types of notifications we recieve if/when a job fails. This way, if a job fails we have the data saved to a database and can export it again once the changes have been made. (AKA if Salesforce API changes, we can continue recieving data from Fulco and do a bulk update once the app is refactored to work with the new Salesforce API specs)

We can write this app in any good web application framework.
My preferences in order are:

1. Laravel (PHP)

*This space exists to demonstrate the concept of "a distant second"*

2. Sinatra (Ruby)
3. Play(Scala)

Competition in the PHP hosting market is significantly higher than the other two, so you are more likely to et better hosting for cheaper with PHP.

Laravel is a very popular web framework among programmers and in the instance that you never want to work with us again or we break protocol and all ride the same flight, which happens to crash, you should have no problem finding a competent Laravel developer who can make edits to the code.

## Estimates:
We estimate this will take us about 70 hours of work