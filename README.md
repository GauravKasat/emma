For finding the best candidate based on a given jd 


Method1 -> Extract jd req and give llm the jd_req and candidate description and ask it to score based on certain attributes. This is heavily dependent on the reasoning capablity of the model


Method2-> Extract jd req and extract candidate useful information and embed them using good embeddings model (see mteb leaderboard for trending embeddings) and find the similarity score using cosine similarity
metric and the candidate with high scores will be more relevant to the given jd

Method3 -> Use keywords based filtering find the number of keywords (present in jd) match  in candidate description . This can work well , However this lacks semantics and lack of understanding of negation.


Out of the 3 methods i will like to go with second method  or hybird combination of method2 + method3 + some heurisitcs rules / filters.

Further scope of improvement
1. Feature engineering -> we can work heavily on doing feature engineering by ourself , rather than relying on llm to calculate (for example total years of exp and other things).

2. We can have an embedding model specifically trained on resume , jd data so that we can have better representation of the data which will basically enhance and add more value to the distance metrics based on which we are finding the relevance.



