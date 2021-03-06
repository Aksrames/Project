# Project
This is the final project for the course Mathematical Techniques in Data Science (MATH 637) at the University of Delaware. The course instructor is Dr. Dominique Guillot. The team members associated with this project are Olivia Mwangi, Desiderio Pilla, and Akshaya Ramesh, who are all students in the Master of Science in Data Science (MSDS) program at UD.

# Abstract

Social media has created a new way for individuals to express their thoughts and
opinions. This medium is used by an estimated 2.95 billion people worldwide,
generating a massive platform for ideas to be shared. Sentiment analysis, or opinion
analysis, is the process of retrieving textual information and discerning which emotions
are exhibited by the author. This type of analysis is used in many ways, including:
determining consumers’ perception of a product, service, brand or marketing campaign;
analyzing a company’s brand recognition on any social networking sites; examining
citizen’s opinions on policy changes, government officials, campaigns, etc.
This project will perform sentiment analysis on real tweets harnessed from Twitter. The
social networking service provides programmers with access to their data through its
APIs (application programming interfaces). The primary aim is to provide a method for
analyzing sentiment scores in noisy twitter streams. This is done by classifying
individual tweets as either negative, neutral, or positive. If a large enough collection of
tweets is analyzed, their collective sentiment score can then be used within a
confidence range to state how the user pool feels towards the specific topic.
In our study, we were able to achieve an accuracy of 77.94% on individual tweet
classifications, and a 95% confidence interval of ± 0.05 on aggregated sentiment score
predictions. The best machine learning method was found to be Stochastic Gradient
Descent. This model was then used on live tweets relating to various subject matters to
extract real-time user sentiment.

# Introduction

The main goal of this project is to build and train a model that can detect the sentiment
of a tweet. For simplicity, this model limit its scope to label all tweets into one of these
three categories:
● negative
● neutral
● positive
Though there are many more specific sentiments that would need to be learned in order
to obtain a clearer picture of a tweet's intentions, we will limit our model to learning
these three classifications. However, a perfect model is nearly impossible to create. The
reason is because sentiment is highly subjective. Roughly 20% of tweets would cause a
debate amongst humans as to which category they fall into . To illustrate this, consider 7
the following two tweets:
I love the world!
I hate the world!
These two tweets clearly fall into the positive and negative, respectively, sentiment
categories. However, consider this tweet:
I am indifferent about the world.
This tweet lies somewhere in between the previous two. Yet, rather than labeling it as
"neutral", one could argue that this in fact elicits a negative sentiment, as it is sad for someone to feel indifferent about the world. In any case, this classification is much less
trivial to assign. Another non-trivial tweet is:
The S&P 500 was down 300 points on Thursday.
This would come as bad news for investors, but happy news for short-sellers. But
broadly, this tweet doesn't seem to have any emotion, but rather only delivers a fact.
Lastly, consider one more tweet:
I love candy, but it has too much sugar in it.
This person begins by saying something positive, but then ends it negatively. Overall, it
is unclear whether this is a net-positive or net-negative tweet. It is also not as bland as
the third example tweet; this sentence exhibits both positive and negative sentiments in
one. The point of these examples is to show that sentiment analysis is not an exact
science, and that this problem has an upper-bound. Even if a model had a 100%
accuracy, humans would disagree with it about 20% of the time. Furthermore, not all
sentiments are as easy to distinguish. A "neutral" label is much more subjective and
poorly-defined than a "positive" or "negative" label.

# Problem Statement

We aim to create a machine learning model that is able to accurately classify the
sentiment of a tweet. "Accuracy" for this model will be defined not only by its ability to
correctly classify individual tweets, but also its ability to correctly classify large quantities
of tweets to create an aggregated sentiment score.
Though the accuracy of the model on individual tweets will be limited by the subjective
nature of this application, we believe it is reasonable to achieve very accurate
aggregate scores. Once a model has been created, trained, and validated, we intend to
use it on real-time and historical tweets to collect aggregated sentiment scores for
varying topics. These can be used to compare real-time responses and attitudes
towards different subjects.
