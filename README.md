Team: Hong Huang, Xinyi Chen, Xintian Shen, Zhihao Yin
# Data-Mining-And-Analysis-In-Movie-Reviews
Data Mining in Rotten Tomatoes Movie Reviews &amp; Sentiment Analysis &amp; Insight of Audience And Critics 

## Dataset
We utilize SELENIUM to accomplish review data crawling from Rotten Potatoes. Mining_critics.ipynb, mining_audience.ipynb and rate_audience.ipynb are used for getting critic reviews, audience reviews and audience grade respectly. 

## Sentiment Anaylsis
Sentiment mining is used for sentiment analysis by senti_final.ipynb. After running this code, we can get sentiment rates, which include 'positive rate', 'neutral rate' and 'negative rate', for every sentences. Then save it into a Excel.

### Linear Regression
From sentiment analysis and audience grade, we get three sentiment grade; combine with audience grade, we use linear regression(linear_regression.ipynb) to explore the relationship between those variables.

<img width="357" alt="uTools_1663053387693" src="https://user-images.githubusercontent.com/97569959/189835508-7f41ea92-b007-40a6-8d41-e5d5fc0fbaa1.png">
Also our model act well by R and R-squared, but we find the relationship between independent variables is high, so the coefficient of association of negative grade is positive.

## Difference between critics reviews and audience reviews 
### Advance word
We choose 3040 words from GRE lexicon as advanced word lexicon. Advanced_words_final.ipynb is used to calculate the the frequency of advanced words from critics reviews and audiences reviews.
Before remove the stop-words(meaningless), the frequance of advanced words for advanced words from critics reviews and audiences reviews is 3.672% and 2.325%; after remove the stop-words, the frequence become 4.933% and 7.499% respectively.
- Critics will use 55% more advanced words then audiences.
- The language form critics is more efficient (less meaningless stop-words)

### LWIC
LIWC is a transparent text analysis program that counts words in psychologically meaningful categories. Empirical results using LIWC demonstrate its ability to detect meaning in a wide variety of experimental settings, including to show attentional focus, emotionality, social relationships, thinking styles, and individual differences.
We use LWIC tool to handle our reviews data, then choose some colums to analyze.

![1663056149166](https://user-images.githubusercontent.com/97569959/189845701-fa5f484c-2064-47a9-a1f2-601353b52761.jpg)
- Critics will use less rate of first person sigular. It indicates critics will show more calm and objective in reviews.
- The rate of conjunctions between critics and audiences have only a small difference, which means the descriptive ability from they is close; but the critics show more stability on this part.
- Critics will use more rate of prepositions and big words (the word with more then 6 letters). It illustrates critics will discuss more complicated informations.
 
## Aspect 
Use tfidf.ipynb to detect which aspect audiences and critics pay more attention to when they judge a movie
![1663058139862](https://user-images.githubusercontent.com/97569959/189853410-f41b715d-c24c-4f82-8537-3a80c39b22be.jpg)
- Audience will discuss more about plot or character when they think it is a bad movie. When they consider it is a good movie, they just start to discuss the acting.
- Critics will pay more attention to comment acting when they accept a moive.
