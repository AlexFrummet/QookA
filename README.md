# QookA <img src="assets/qooka_logo.png" alt="QookA logo" width="40"/>
This repository accompanies the paper **QookA: A Cooking Question Answering Dataset**.

## Where is the dataset?
The dataset is stored in the `qooka_dataset.csv` file.

## What do the columns mean?
- `global_turn_id`: A unique identifier for each turn, combining the conversation ID and the turn ID in the format <conv_id>_<turn_id>, e.g., 10_4 

- `query`: The recorded and transcribed query issued by a crowdworker, e.g., "How much sugar do I need to add?"

- `answer`: The answer to the query, e.g., "200g"

- `alternative_answer`:  Sometimes, multiple answers are plausible. If multiple alternative answers exist, they are separated by a `|` delimiter, e.g., "1 cup|7 oz" 

- `level_0_query_need`: The cooking information need label at level 0, according to Frummet et al.'s taxonomy (see [codebook](https://github.com/AlexFrummet/CookversationalSearch/blob/master/annotation/annotation_schema_cookversational_search.xlsx) and [info. need tree](https://github.com/AlexFrummet/CookversationalSearch/blob/master/annotation/InfoNeedTaxonomy.svg)), e.g., "fact"

- `level_1_query_need`: The cooking information need label at level 1 according to Frummet et al.'s taxonomy (see [codebook](https://github.com/AlexFrummet/CookversationalSearch/blob/master/annotation/annotation_schema_cookversational_search.xlsx) and [info. need tree](https://github.com/AlexFrummet/CookversationalSearch/blob/master/annotation/InfoNeedTaxonomy.svg)), e.g., "amount" 

- `is_exact_query_answer_match`: True if the query exactly matches with the highlighted word, and false if not.

- `is_internal_knowledge_source`: True if the answer is found within the recipe, and false if not.

- `is_reasoning`: True for yes/no questions and reasoning that requires background cooking knowledge. For example, "Can I use a normal spoon as well?" is true; false if not.

- `recipe_id`: The recipe ID that the current turn is referring to, e.g., 49

- `recipe_title`: The title of the recipe that the current turn is referring to, e.g., "Thai Spicy Duck Salad Recipe"

- `step_number`: The step number the query is referring to, e.g., 1

- `conv_id`: The conversation ID the query is referring to, e.g., 10

- `turn_id`: The turn ID within the current conversation, e.g., 4

## Citation
When using this dataset, please have look at [our paper](https://dl.acm.org/doi/10.1145/3627508.3638311) and cite us :-)
```bibtex
@inproceedings{frummet2024qooka,
  author       = {Alexander Frummet and
                  David Elsweiler},
  editor       = {Paul D. Clough and
                  Morgan Harvey and
                  Frank Hopfgartner},
  title        = {{QookA: {A} Cooking Question Answering Dataset}},
  booktitle    = {{Proceedings of the 2024 {ACM} {SIGIR} Conference on Human Information
                  Interaction and Retrieval, {CHIIR} 2024, Sheffield, United Kingdom,
                  March 10-14, 2024}},
  pages        = {406--410},
  publisher    = {{ACM}},
  year         = {2024},
  url          = {https://doi.org/10.1145/3627508.3638311}
}
```

