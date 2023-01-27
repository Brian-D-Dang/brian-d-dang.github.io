---
layout: essay
type: essay
title: "Questions, how to ask em"
# All dates must be YYYY-MM-DD format!
date: 2023-01-26
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/stackOverflow.png">

StackOverflow is known as a developer’s best friend. Whenever you run into specific coding problems, StackOverflow would usually have an answer. Interestingly enough many developers also never have to ask questions, but when they do many developers may not understand how to ask. In this essay we will talk about bad questions and. smart questions

## What’s a bad question?

Bad questions are easy to ask. If you don’t take the time to expand upon your problems you can  easily ask a low detailed question which often gets ignored. An easy way to ask a bad question is by “guessing” issues instead of “describing” the symptoms of your problem. Bad questions also lack explicitly, as I stated earlier. Bad questions often contain low detail and aren’t explained well enough to help the reader understand your problem/question. It also makes it less appealing to help, as you have little to no information to build off of.

An example of such a bad question can be found below:
<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/badQuestion1.png">

## What's a smart question?

Smart questions on the other hand are a lot harder to ask as they require more time to develop. To ask smart questions first begins with being detailed in your problem/question. Explain the symptoms of your problem, and showcase code that is necessary and tied to the area you’re trying to solve/fix. Adding this level of detail to your question creates a more inviting question, which leads to more help. 

An example of smart question can be seen below:

<div class="text-center p-4">
  <img width="800px" 
       src="../img/smart-questions/goodQuestion1.png" 
       class="img-thumbnail" >
  <img width="800px" 
       src="../img/smart-questions/goodQuestion2.jpg" 
       class="img-thumbnail" >
  <img width="800px" 
       src="../img/smart-questions/goodQuestion3.png" 
       class="img-thumbnail" >
</div>

## Conclusion

Looking at both questions we can also see the amount of traction each question received. The bad question received 0 comments and -1 likes, while the smart question received 26861 likes and many comments. When you can’t find a solution to your problem, and your last resort is StackOverflow, then you should take the time to develop smarter questions and to add in the necessary details to help the reader understand. It will have a more likely chance of a reader responding and being helpful.


```
Q: python date of the previous month

I am trying to get the date of the previous month with python. Here is what i've tried:

str( time.strftime('%Y') ) + str( int(time.strftime('%m'))-1 )

However, this way is bad for 2 reasons: First it returns 20122 for the February of 2012 (instead of 201202) 
and secondly it will return 0 instead of 12 on January.

I have solved this trouble in bash with:

echo $(date -d"3 month ago" "+%G%m%d")

I think that if bash has a built-in way for this purpose, then python, much more equipped, should provide something 
better than forcing writing one's own script to achieve this goal. Of course i could do something like:

if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
        
I have not tested this code and i don't want to use it anyway (unless I can't find any other way:/)

Thanks for your help!
```

While the heading of his question could be better, it does convey what he’s trying to figure out. Usually something as brief as “python date of previous month” is what other users would enter in as search terms on Google, making it easily found. Another good thing about the question is that it’s not just a question. The asker shows what he or she has done and that he or she has put in some effort to answer the question. And while it may not be as important as the question itself, the asker shows courtesy, which does increase the chance of getting an answer.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
