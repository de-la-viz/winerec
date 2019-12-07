# #winerec, A Content-Based Wine Recommendation System Using Professional Tasting Descriptions

*“There are thousands of wines that can take over our minds. Don't think all ecstasies are the same!”― Jalaluddin Rumi*

How to select wine so that it matches your taste best? Data science can be used to solve this problem with a recommendation system, which propose wines that the user is expected to like.

There are two main types of recommendation systems: collaborative filtering recommends wines based on matching users with similar past interest (“wisdom of the crowd”) and content-based filtering recommends similar wines to the ones each user liked in the past. 

What if we have no history of user interactions with the recommender system? We face a *cold start problem* and it is impossible to build a (truly) collaborative filtering recommendation system. It is easier to start with content-based filtering, by starting with basic user profiles and build the profiles with time. The recommendation system can later make use of the user profiles to slowly introduce some collaborative filtering.

I thus decided to build a content-based wine recommendation system, but what are the “contents”? The “contents” are attributes of the wines previously liked by the user. So, how do you choose your wine, what attributes do you search for? 

* You might look at the style of bottle label or the price. The importance of these two factors is not to be downplayed, however they are not directly related to taste. 

* You might look at ratings proposed by shop owners, wine experts, or even other wine enthusiasts (e.g. Vivino). However, the fact that everyone has different tastes allows only for limited customer tailored recommendations (remember that we are not in the position to use collaborative filtering recommendation due to the cold start problem). It also discourages diversity since it steers the global winemaking towards producing a homogeneous style in order to appeal to the mainstream critics.

* You might search for wines from a known variety or origin. Those are important for taste, but despite coming from the same region or being made with the same grapes, wines can vary substantially in taste, aromas and structure, due to subtle differences in the local terroir, winemaking process or vintage. It also goes without saying that this strategy will not allow to broaden your horizons and discover wines previously unknown to you.

**To date, a source of data that has been largely overlooked for wine recommendation solutions are tasting descriptions. Text descriptions written by professional sommelier aim precisely at describing the subtle differences in taste, structure or aromas between the wines, using an elaborate vocabulary.**

**This project is a proof of concept, which aim is to test the assumption that professional wine reviews can/should be used for wine recommendations. Thus, I will try to build a recommendation system using only the tasting descriptions. In a real application, we might want to use other “contents” too.** I will follow four steps:  
1. Use Natural Language Processing (NLP) to extract the information contained in the descriptions
2. Build a content-based wine recommendation system using these tasting descriptions
3. Recommend wines based on one selected wine that the user liked (i.e. initial profile of the user)
4. Try to evaluate the recommendations (difficulty: unsupervised learning)  


**The project is presented, commented and discussed in this [presentation](https://docs.google.com/presentation/d/1tCcIGw24lLizHxUUMnMihTvOzKZYvRUpyS5TRDJtqBU/edit?usp=sharing).**

**[This notebook](https://github.com/de-la-viz/winerec/blob/master/code/WriteUp.ipynb) contains the code for building the recommendation system and presents the different steps and the process.**  

Techniques used: unsupervised learning, natural language processing, word embeddings and topic modelling (pandas, numpy, scikit-learn, spaCy, word2vec, LDA, pyLDAvis, tf-idf, cosine similarity)
