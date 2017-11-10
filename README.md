# data512-a3 Project Plan

Building a recommendation engine for Redditors
Abhishek Varma

ABSTRACT:

Using publicly available data that Redditors have made available on the website through Amazon wishlists, I am able to build a recommendation engine that suggests gifts for redditors by matching them with similar redditors already present in our database. The Redditors who match will have an option of being able to message each other since they have shared interests. As the site grows, my aim is to see if more Redditors volunteer their info to the site to share gift ideas that they find cool for their own ‘reddit twin’.

BACKGROUND

I was recently exploring Japan and getting lost in the wonderland that is Tokyo. In some bar (my memory is a little hazy) I encountered a local and we chatted over some whiskey. We found that we had a lot of shared interests and he recommended I go to a particular manga shop and get the enlish version of a particular manga, one that I had never heard of. I went ahead and bought one for myself and absolutely loved it. I realized that had I not met that person in this dive bar in Tokyo, I would never have been able to find this manga. That is the experience that inspired me to work on this project. 

 One of the most interesting applications of machine learning to me is the recommender system. As we gain access to an exponentially large database of content and data on the internet, we can sometimes get lost and never find anything new. We will listen to the same songs, watch the same movies and buy the same gifts. When looking at the runaway successes of Facebook and Amazon, it is clear to see that they are so popular in the online marketplace because they have a lot of personal information about their users. Reddit, on the other hand, does not. 

All you need to open a Reddit account is a username and password. However, my hypothesis is that as you open up more on an online ‘anonymous’ forum, the context of where you posts can help paint a picture about your personality and interests. I aim to research if this context can be used to suggest gifting ideas to each other and to even see what kind of items people like you are buying as a way to gain exposure to goods that we may never gain exposure too.

DATA

There is a subreddit called Random Acts of Amazon (www.reddit.com/r/raoa) where redditors publish their amazon wishlists and other redditors gift them things from the wishlist. There are around 800 users in the database and inactive users on the subreddit are dropped from the database after 30 days of inactivity. The database is available online and all the information is voluntarily provided by the users of the subreddit.

After contacting the mods or r/raoa, I was able to gather an SQL dump of the latest database. This data is just a list of SQL insert queries and is available publicly on the web. I have the permission to use this data for this project from the mods. There is also a terms and conditions page on the subreddit that states that the wishlists that are provided on the subreddit will draw a relationship between your reddit username and Amazon account. Indeed, if this information was not public, the whole point of the subreddit would be negated. Once the tool is published, I want to observe how many more people volunteer more information and see how our dataset can grow with a non comercialized crowdsourcing approach.

I plan on using Python to extract the data itself from the SQL dumps so that it is easier to manipulate. I will maily use Pandas to store the data as it is not very large. I will use the Python Reddit API to access the Reddit usernames.

METHODOLOGY

I plan on creating using a jaccard similarity model to measure the similarity between the user of the tool and the existing database of redditors. My theory is that reditors who comment on similar subreddits will have similar tastes. I will normalize the data by removing the default subreddits so that only the subreddits that someone has actuvley commented on turns up in the data. This way we will be able to identify the unique combinations of subreddits and the jaccard similarity will nto be lost be everyone commenting on the same default subreddits.

Human Centered Approach

I want to encourage people to reccomend things to complete strangers and observe if the gratificatin of finding cool stuff creates the same kind of bond that I felt with my Japanese wanderer. I also want to observe if the gratification of sharing things and getting positive feedback is incentive enough to crowdsource a dataset. 

