# Gender Bias Measurement of Information Retrieval
This repository contains the resources and code for measuring gender bias in the result list of Information Retrieval models, as explained in the paper: https://arxiv.org/abs/2005.00372

## Resources:
- `resources/queries_gender_annotated.csv`: Annotation results of the related gender of queries.
- `resources/wordlist_genderspecific.txt`: List of gender specific words.

## Code
#### Step 1 : calculating bias for the collection's documents
Follow the code in `step1_calculate_bias_documents.ipynb` for calculating the gender bias of each document in collection. At the beginning of the notebook, set `collection_path` to the path of the collection with TSV format. For MS MARCO collection, this should refer to the `collection.tsv` file. The code does not apply any particular pre-processing to the text unless converting it to lower case. It is suggested that you apply the required pre-processing before hand.

#### Step 2 : calculating bias for TREC run files
Using the pre-calculated document biases, `step2_calculate_bias_runs.ipynb` calculates gender bias scores for each query for the given retrieval run files. 

#### Step 3 : RaB and ARaB metrics
- `step3_bias_metrics.ipynb` calculates the final gender bias metrics for each experiment.

### Reference
The paper will appear in the proceedings of SIGIR 2020. Reference to the arXiv version:
```
@inproceedings{rekabsaz2020neural,
    author = {Rekabsaz, Navid and Schedl, Markus}, 
    title = {Do Neural Ranking Models Intensify Gender Bias?}, 
    year = {2020}, 
    doi = {10.1145/3397271.3401280}, 
    booktitle = {Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval}, 
}
```
