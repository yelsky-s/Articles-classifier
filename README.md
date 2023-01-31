# Articles-classifier
 Scientific publications usually specialize in a relatively broad topics, like internal medicine, partical pfysics, biology etc. Readers of those publications are often interested in a narrower subject of a respective topics (which can be subcategorized further).
  This project attempts to sub-categorize a broader geoscience publications topicsfrom 2 publications: Geology and Jornal of Hydrology, based on each individual article's abstract it recent issues of those jornals. 
  Algorithm uses python NLTK and Gensim (LDA - Latent Dirichlet Allocation) packages.

Article from web_classifier.ipynb file: 
 The abstracts were abtained from the web by the means of webscraping with Requests and BeautifulSoup. Te abstract text then is proccessed and tokenized using Python NLTK library.
 
 ****

article classifier.ipynb  file:

Classification of geological articles to sub-categories.
This file takes a pdf article from scientific journals on geology and classifies them into one of 4 subcategories: hydrology, earthquakes, tectonics or non of the above. Text processing in this script was done with NLTK library using costumised themes lists for each category: hydrology, earthquakes and tectonics. In this app the work with PDF files was done using PyPDF2 package. 

Example of a classifier outcome of an article named - Evaluation of a Ground Water Potencial using Aquifer Characteristics on Parts of Boki Area, South Eastern Nigeria -> Article 1 in this repository.
![image](https://user-images.githubusercontent.com/101993270/159779191-9ca31e34-a73e-4376-8522-b0a139e1aa60.png)

Another example for a PDF article on fashion consumption and sustainability (listed in a repository as Article 2)
![image](https://user-images.githubusercontent.com/101993270/159779463-76d40ce8-62b5-4aaa-8771-93bac78d5e0b.png)
