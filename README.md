## This web scraper was built to scrape text from [parler.adatascienti.st](https://parler.adatascienti.st/) who archived the data that was scraped from Parler in January 2021 and made it publicly available. 
I would like to thank [a data scientist](https://twitter.com/anonymousdata_) for creating the search capability that my scraper uses to pull posts based on certain sentiments. 

## Background on Threat Detectives
The inspiration for this project came after the January 6th Capitol Riot. We wanted to create a tool that would look for similar language to what was being said on Parler, in the time leading up to the insurrection, in an effort to raise an alarm on future civil unrest.

We knew the Parler data was saved into a Docker container, but the container was over 50TB of data and nobody on my team had that kind of space on their machine. 

I searched and waited for someone to make the data publicly accessible but we eventually started running out of time and had to find a different dataset to train our Threat Detective model on. 

Now, I am finally able to deliver the sentiment analysis model that I originally wanted, trained on the data scraped from Parler. 
