# File-Search-Engine

- This is python based search engine for text files. It searches through various text files to search for particular phrase provided by user.
- It is implemented in 3 steps:
  - Indexing,
  - Phrase Search and
  - Ranking
 
## Features:
-  Ignores indexing of words present in stopword.dat because they are commonly used words.
- Stemming of words is done with help of Porter Stemmer to ignore different types of verbs.
- It has options for free text query (both one word and multi word queries) and phrase query. For phrase query put query in double quotes.
- It prints file name and lines having the query.
- It ranks the documents on basis of OKAPI BM-25.

## How to run?
```
python createindex.py stopwords.dat indexOut.dat filename.dat
```
It will ask for path to the folder having the files to be indexed. Give the path and words in all the files will be indexed in indexOut.dat file. Now, if you want to search for query you can do so or you can quit by pressing enter key. Now, if you want to search again (but you don't want to index again because that takes time) you can run following command.

```
python queryindex.py stopwords.dat indexOut.dat filename.dat
```	
It will again ask you for path to the folder having the files that were indexed. You would get filename, line number in that file and line having query you searched for.

Here is screenshot for your reference. It shows result for multi word free text query.
screenshot 


