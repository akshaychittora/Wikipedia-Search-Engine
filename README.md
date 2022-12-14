# Wikipedia Search Engine
This projects implements a query processing system for wikipedia page retrieval which will include both
hindi and english pages and query can also be in english and hindi both languages. User can search for
any information by passing query in form of keywords or a phrase, It then searches for relevant information
in its database and returns relevant results to the user, wikiepdia article links. The query can be fired in terms of fields or just as simple query.
For simple query the keywords were matched based on all the fields of the pages.
First, preprocessing is done on the XML file, Tokenization, stop word removal and stemming then Creating the intermediate index, 
creating final index using this intermediate index and finally creating posting list for each word using the final index.

The query given is parsed, processed and given to the respective query handlers . For Hindi query, we use transliteration to convert English text to Hindi script which will work both ways for direct hindi words as well as indirect.
One by one word is searched in vocabulary and the file number is stored.
The respective field files are opened and the document ids along with the frequencies are fetched.
The documents are ranked on the basis of TF-IDF based cosine similarity scores and are also weighted on the occurrence in title, body, category, etc.


## File Structure:
`english_indexer.py` : Used for creating indexes for the english language dataset<br>
`hindi_indexer.py` : Used to create indexes for hindi language dataset <br>
`hindi_stem_words.txt` & `hindi_stop_words.txt`: Contains data for preprocessing<br>
`Query_runner.ipynb` : Notebook containing code for query processing and examples

## Link to Dataset:
 Link to English dumps: https://dumps.wikimedia.org/enwiki/20220420/
Link to Hindi dumps: https://dumps.wikimedia.org/hiwiki/20220420/

## Steps to run:
##### Create `english_wiki_index` and `hindi_wiki_index` in the same directory as indexer files to run them.<br>
For english indexing : `python3 english_indexer.py --input input_dataset_in_xml`<br>
For hindi indexing : `python3 hindi_indexer.py --input input_dataset_in_xml`<br>
These will create the necessary index files.

For Query Processing: Run the `Query_runner.ipynb`. run_query() function gives information about using the function.
