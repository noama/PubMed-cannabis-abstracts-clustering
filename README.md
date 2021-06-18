 # Explore the knowledge and trends of cannabis research </br> using K-means clustering and text analysis

<p>
This repository contains an implementation of a K-means clustering for grouping PubMed abstracts in cannabis field into categories that reflect the core themes in the existing studies and also examine the trends of cannabis research during the last 20 years.
</p>

<p>
  
</br>

##### This repository contains the following files:
1. <i>pubmed_cannabis_dataset.nbib</i> – This file contains the results of our search query - PubMed abstracts in cannabis field. Each result cotain and also other fields such as title, author, publication date and etc. This file was downloaded directly from PubMed.</br>
2. <i>cannabis_abstract_clustering.ipynb</i> – This jupiter notebook read the nbib file -pubmed_cannabis_dataset.nbib. The text is split to extract the fields to dataframe using nbib library. The dataframe has been cleared of unnecessary fields. The abstract field has been cleared, tokenized and stemmed using NLTK and than transformed into tf-idf feature matrix using Scikit-learn. Finally, K-means is used to cluster the abstracts.</br>
3. <i>stopwords_costum.txt</i> – In addition to NLTK stop words that conlude set of commonly used words in English i.e. “the”, “is” and “and”, we also create a list of stop words for our corpus. In our corpus, words like “abstract”, “background”, “results” and “conclutions”  occur almost in every abstract. So, we use this file to eliminate these unimportant words and thus allow to focus on the important words instead.
</p>

<p>
In addition, we also attached files at various processing stages. Using these files can save the running time of early stages.</br>

##### These files are optionally:
1. <i>optional_files/cannabis_abstracts_clean.csv</i> – clean dataset in csv format.</br>
2. <i>optional_files/finalized_kmean_model.sav</i> – This file contains the kmean clustering results of 20 models. The runtime of this step can take about 15 minutes on a PC. Using this file will reduce the runtime. </br>
In addition, using this file will display results that match the descriptions of the results shown in the notebook. When using k-means, we can get different clustering results. set the random_state parameter ensures that different runs will start at the same points but its not ensures that we’ll get consistent results. We run the k-mean algorithm in our dataset many times, and we noticed that the main trends that we mention on our results are consisted in all runs. This indicates that the data cluster well with k-means.
3. <i>optional_files/abstract_by_cluster.csv</i> – clean dataset with new columns - ‘category’ that contain cluster label.</br>
</p>

### Results

![results](https://user-images.githubusercontent.com/86036130/122510501-5dfe5280-d00e-11eb-93d0-9aa29433a14d.png)

### This project was done in collaboration with Michal under the guidance of Itamar as part of the course - "Introduction to Data Science - Tools and Methods" offered by Campus IL and SCALE-UP.
