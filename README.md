# Wiki_SearchEngine
This is a search engine built on the full English corpus of wikipedia (~75GB)

Performance
For Queries Of
less than 3 words, time to fetch results is < 1s
between 3 and 7 words, time to fetch results is Around 5s

Code Files
myWikiIndexer.py - File containing all functions related to XML parsing and text preprocessing, the code for indexing.
k-way-merge.py - File with functions related to k-way mergesort algorithm and creates secondary index.
search.py - Main file containing all the code for Query Processing


Execution of Code
Prerequisites
Required Directories
index - Initial index gets created here
finalIndex - They get merged here and also stored secondary index in this directory

Required Files
stopwords.txt - A txt file containing all the stop words in the current directory of the code
wiki_dump.xml - The XML file containing the full data of wikipedia

Execution
Run myWikiIndexer.py with path to dump and folder to index as command line arguments.
Run k-way-merge.py - Will sort the index and create secondary index
Run search.py - An infinite loop runs expecting queries.

Types of Queries
Normal query - Any sequence of words that doesn’t satisfy the above conditions is considered a normal query eg: “Sachin Tendulkar”
Field query - Assuming that fields are small letters(b, i, c, t, r, e) followed by colon and the fields are space separated. eg: “body:sachin infobox:2003 category:sports”
