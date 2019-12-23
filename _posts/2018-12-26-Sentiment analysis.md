---
layout: post
title: Sentiment Analysis
subtitle: ...making a machine understand sentiments
image: /img/sentiment/cover.png
---

People's Choice Award is an annual award show on E! Network voted on by the people and, hopefully, the nominee suggestions are fully representative of the people. How can these suggested nominees are representative of the people as they are so beautiful and rich and we hardly know them even to vote? To many people's surprise, given the rising role of data science in many industries including media, the nominee suggestions are completely backed by data and each nominees are evaluated from various perspectives such as consumption (e.g., Box Office's Gross) and social impact (e.g., Instagram's number of followers, Twitter's sentiment). 

My internship at NBCUniversal aimed to develop a metric to evaluate social impacts of TV shows and programs, using Twitter's tweets provided by Nielson Social. A simple correlation anlysis between show performance (i.e., IMBD impressions) and conversation volumes (i.e., number of teets) quickly helped me realize that conversation volumes tell little, if nothing, about audience's interest in TV shows. For example, Game of Thrones is #1 tweeted TV show but for both groups of demo people at all age, and people from 18 to 45 years old, there is no correlation between IMBD impression and the volume of conversation. As a result, sentiment analysis plays a vital role in evaluating social impacts of TV shows. 

The first step was to select the "right" data by reasoning and by exploration. At first, I wanted to run the sentiment analysis on multiple TV shows using program-level data (e.g., tweets about each programs, regardless of episodes) and learned that this provided only few insights on audience's opinions about the show, espeically if the audience is widely distinguished across episodes. Failing to go broad, I decided to go deep by looking at episode level data and this also meant I could only look at most three shows, given the time constraint. With help my manager's domain experitise, I selected three shows to cover a wide range of styles: The Tonight Show Starring Jimmy Fallon (Semi-scripted late night show), American Idol (non-scripted, competiton), and Game of Thrones (scripted). 

The right data needed a lot of preprocessing and cleaning work to avoid "garbage in, garbage out." 




<!-- ![alt text](/img/Sentiment/ratings.png) -->


 
<!-- I have put the code on [GitHub](https://github.com/Regressionist/Sentiment-analysis). You can refer to this code if you want to know how to convert a pandas dataframe to a torchtext tabular dataset. <br/>
Merry Christmas everyone!

Thanks,<br/> -->
<!-- Ashwin -->