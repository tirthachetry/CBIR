# CBIR
The 4 Steps of Any CBIR System
No matter what  **Content-Based Image Retrieval System** you are building, they all can be boiled down into 4 distinct steps:

1).Defining your image descriptor: At this phase you need to decide what aspect of the image you want to describe. Are you interested in the color of the image? The shape of an object in the image? Or do you want to characterize texture?

2)Indexing your dataset: Now that you have your image descriptor defined, your job is to apply this image descriptor to each image in your dataset, extract features from these images, and write the features to storage (ex. CSV file, RDBMS, Redis, etc.) so that they can be later compared for similarity.

3)Defining your similarity metric: Cool, now you have a bunch of feature vectors. But how are you going to compare them? Popular choices include the Euclidean distance, Cosine distance, and chi-squared distance, but the actual choice is highly dependent on (1) your dataset and (2) the types of features you extracted.

4)Searching: The final step is to perform an actual search. A user will submit a query image to your system (from an upload form or via a mobile app, for instance) and your job will be to (1) extract features from this query image and then (2) apply your similarity function to compare the query features to the features already indexed. From there, you simply return the most relevant results according to your similarity function.

#### Download Dataset folder from the below link: <br/>
> https://drive.google.com/open?id=1Wt0-p42pc1FvBysFX-9Ojg01aqg_KteG

# Following Steps For Using
Open up your terminal, navigate to the directory where your code lives, and issue the following command:<br/>
> python search.py --index index.csv --query queries/input.png --result-path dataset

# Note
Input the image name given in the queries folder as input.jpg



# References
1) https://www.pyimagesearch.com
2) https://opencv.org
3) http://fab.cba.mit.edu/classes/865.15/people/desmond.lim/project-06.html
