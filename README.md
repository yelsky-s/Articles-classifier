# Articles-classifier
 Scientific publications usually specialize in a relatively broad topics, like internal medicine, particle physics, biology etc. Readers of those publications are often interested in a narrower subject of a respective topics (which can be subcategorized further).
  This project attempts to sub-categorize a broader geoscience publications topicsfrom 2 publications: Geology and Journal of Hydrology, based on each individual article's abstract it recent issues of those journals. 
  Algorithm uses python NLTK and Gensim (LDA - Latent Dirichlet Allocation) packages.

Article from web_classifier.ipynb file: 
 The abstracts were obtained from the web by the means of web scraping with Requests and BeautifulSoup. Articles were summarized using Pegasus model (a transformer abstractive summarization with a pretrained model from HuggingFace website). Below, 2 examples of a summaries are shown alongside articles abstract and title.
![image](https://user-images.githubusercontent.com/101993270/217833368-1639e85e-d913-4e2c-8b42-f565761d3474.png)
![image](https://user-images.githubusercontent.com/101993270/217833990-369683a2-a48c-4f38-9290-396f32221765.png)
 
 The abstract text then is processed and tokenized using Python NLTK library.

Model was built with num_topics parameter equal to 4.
![image](https://user-images.githubusercontent.com/101993270/216041258-5ff39104-4a8d-4c02-b6c1-fcc27b3b36d5.png)
Out of the classified articles, the model detected 43 that belong to cluster 1, 40 to cluster 2, 29 - cluster number 3 and 40 to cluster 4.

Visualization of the LDA model results was made using pyLDAvis.gensim_models. Below metrics for topic 2 is shown:
 ![image](https://user-images.githubusercontent.com/101993270/216041021-b6622320-78a7-4033-a043-73bfea9e4ef7.png)

And here is part of the table with articles that was clustered into topic number 2:
![image](https://user-images.githubusercontent.com/101993270/216043463-271cf286-b0a8-45b2-81ce-48ef07371886.png)

 ****

article classifier.ipynb  file:

Classification of geological articles to sub-categories.
This file takes a pdf article from scientific journals on geology and classifies them into one of 4 subcategories: hydrology, earthquakes, tectonics or none of the above. Text processing in this script was done with NLTK library using customized themes lists for each category: hydrology, earthquakes and tectonics. In this app the work with PDF files was done using PyPDF2 package. 

Example of a classifier outcome of an article named - Evaluation of a Ground Water Potential using Aquifer Characteristics on Parts of Boki Area, South Eastern Nigeria -> Article 1 in this repository.
![image](https://user-images.githubusercontent.com/101993270/159779191-9ca31e34-a73e-4376-8522-b0a139e1aa60.png)

Another example for a PDF article on fashion consumption and sustainability (listed in a repository as Article 2)
![image](https://user-images.githubusercontent.com/101993270/159779463-76d40ce8-62b5-4aaa-8771-93bac78d5e0b.png)
