# Wikipedia Search Engine
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
