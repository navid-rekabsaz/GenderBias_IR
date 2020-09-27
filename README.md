# Gender Bias Measurement of Information Retrieval
This repository contains the resources and code for measuring gender bias in the result list of Information Retrieval models, as explained in the paper: https://arxiv.org/abs/2005.00372

## Resources:
- `resources/queries_gender_annotated.csv`: Annotation results of the related gender of queries.
- `resources/wordlist_genderspecific.txt`: List of gender specific words.

## Code
- `documents_calculate_bias.ipynb`: The code for estimating the gender bias of each document in collection.
- `runs_calculate_bias.ipynb`: Using the document biases, this notebook calculates various gender bias values for each query in a given retrieval run file.
- `model_calculate_bias.ipynb`: Final retrieval gender bias measures are calculated in this code.

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
