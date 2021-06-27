# These instructions are meant to break down how to label the scraped Parler text data and what to do with it next. 

## ========= How to Label the data =========

- The top of every file needs to have the following text:
`Post,Threatening,Conspiracy,Hateful,Neither`
- Remove any commas(`,`) from the post.
- At the very end of a single post, type a comma(`,`) and then begin your labeling.
- You're going to follow that comma with 4 numbers (either a 1 or a 0), seperated by commas like this:
  > Here is my post,0,0,0,1
- a 1 is affirmative and a 0 is negative 
- The four numbers at the end of the post refer to the columns:
 **Threatening,Conspiracy,Hateful, or Neither**
  - Read the post and get a good "feel" for it.
  - You should label each column according to if the post is either threatening, conspiracy-speech, hateful language, or neither(neutral).
  - Each post should only have a single 1 label and three 0 labels. We don't want to confuse the model by teaching it the same text can mean two different sentiments. We have to be more specific than that in this case.
  - If the post doesn't fall in any of those categories, delete it from the file. We don't need it. We can always scrape more data if we need to.
  - Delete any duplicate posts
- Delete all dates or anything else that is not part of a post.
- Delete any full rows of whitespace. Each post should have it's own line number.
- I have labeled the first 5 post of [posts_loser.csv](./posts_loser.csv) to give you an example. 

## ======== Sentiment Definitions =========
### Conspiracy:
  - Relating to Qannon/Antifa conspiracies
  - Election Fraud
  - Trump as god/leader/savior
  - Fake News/Fake Media
  - Chinese Virus
  - Anti-mask/anti-vaccine

### Hate Speech:
  - If the post is talking shit about someone or a group of people, it is hate speech
  - Name calling
  - Accusing a person or group of people of doing something bad
  - Racial slurs
  - Racists, homophobic, transphobic, misogynist comments are all hate speech

### Threatening:
  - Exclaiming they will do something negative to another person or group of peoples
  - Talking about using weapons
  - Trying to find someone's location
  - Talking about stopping someone from doing something 
  - Talking about causing harm to someone or group of people
  - Talking about killing anything or anyone(s)

### Neither:
  - The post doesn't fit the other three catagories.
  - The post has a more neutral sentiment.
  - The post doesn't have any other kind of obvious sentiment that isn't listed.

## ======== Move the finished file  =========
- When finished labeling and modifying the file:
  - Save it!
  - Drag the file to the `parler_dataframes` folder
  - Once we are ready to incorporate this new data, I will copy over the whole folder to the repo where the model is being trained at. 
  - When you finish with a file, please ACP your work so that I can test the csv file to make sure it works with Pandas

# Thank you, Ryan!! Let me know if you have any questions!