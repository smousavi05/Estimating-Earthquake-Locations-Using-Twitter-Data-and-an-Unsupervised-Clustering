# Estimating Earthquake Locations Using Twitter Data and Affinity Propagation

-------------------------------------
S.Mostafa Mousavi

Seismographs (instruments used for recording seismic signals) continuously record velocity of ground motions at different locations. When the ground shaking at a particular seismic station exceeds a predefined threshold, a seismograph gets triggered and transmit an alert to a data center. Triggering of multiple instruments at different stations over an area within a relatively short period of time usually indicates the occurrence of an earthquake. The transmitted seismic signals from multiple stations need to be processed further to estimate the earthquake hypocenter.

![ovel view of seismic wave propagation](F0.jpg)

However, this process can be time-consuming (takes a few to several minutes) and moreover there are many places around the world with not a good coverage of seismic stations. 

The main idea here is to use the first order reports of an earthquake occurrence in the social media by people who actually felt it, for a rapid/rough estimation of earthquake location. Due to the speed of post creations and ease of near real-time access, using social media such as Twitter can be a potential for gaining situational awareness following disasters.

Here I present a simple way to do this without any need for steam of the data or NLP or training data set.

-----------------------------------------

# Part 1: Getting the Twitter Data

You need to create an account for Twitter API first and use your consumer and access information for connecting the Twitter API. (here I deleted mine!)


we search Twitter API for the word "earthquake" in 23 different languages:
 
To retrive dat from Twitter we first need a tweet Id as a 'starting point' from which to search. 
`get_tweet_id()` function finds the ID of a tweet that was posted at the end of a given day.

Twitter limits the maximum number of tweets returned per search to 100. 


-------------------------------------------

# Part 2: Getting the Earthquake Data 

Again there are several ways for doing this using different options for downloading earthquake catalogs from international data centers such as ISC (http://www.isc.ac.uk/), using national catalogs like comcat, using official API of Us Geological Survey, or accessing to different apps. 


to search for the earthquake information for the same time period and then retrieve the data and store it in a local directory. 

________________________________

# Part 3: Analyzing the Downloaded Data
Our goal is to detect earthquakes based on evidences of firsthand felt reports from Twitter. So we need to identify tweets originating from users who experienced earthquake shaking like this one:

![the tweets we are looking for](F.png)



Filtering tweets with these keywords out, we archive the tweet creation time, text, and coordinates into a dataframe.

----------------------------------

# Part 4: 3D Clustering

After filtering of the Twitter data,a clustering incorporating temporal/spatial dimension of the data can further help us in identifying earthquake activities. 


-----------------------------------------

# Part 5: Results



Not bad, yeah

