<!-- SPACY PROJECT: AUTO-GENERATED DOCS START (do not remove) -->

# 🪐 Prodigy / spaCy / wandb pipeline based on 🪐 spaCy Projects
## Use Case 01 NER BBC & NG news
+ Annotation process via Prodigy annotation tool
+ Weights & Biases for logging of training experiments


NER project for spaCy v3. The project data comes from kaggle: 
+ BBC (https://www.kaggle.com/hgultekin/bbcnewsarchive)
+ NG (https://www.kaggle.com/salmaelanigri/doc-class)

Label scheme (2 labels for 2 components):

| Component | Labels |
| --- | --- |
| **`NER`** | `PERSON`|
| **`ENTITY_RULER`** | `EMAIL` |

## 📋 project.yml

The [`project.yml`](project.yml) defines the data assets required by the
project, as well as the available commands and workflows.

### ⏯ Commands

The following commands are defined by the project. They
can be executed using [`spacy project run [name]`](https://spacy.io/api/cli#project-run).
Commands are only re-run if their inputs have changed.

| Command | Description |
| --- | --- |
| `data-to-spacy` | Merge your annotations and create data in spaCy's binary format |
| `train_spacy` | Train a named entity recognition model with spaCy and log the results via wandb |
| `train_prodigy` | Train a named entity recognition model with Prodigy |
| `train_curve` | Train the model with Prodigy by using different portions of training examples to evaluate if more annotations can potentially improve the performance |
| `evaluate` | Evaluate the model and export metrics via spaCy |
| `visualize-model` | Visualize the model's output interactively using Streamlit |
| `visualize-data` | Visualize the data interactively using Streamlit |
| `package` | Package the trained model so it can be installed |


### ⏭ Workflows

The following workflows are defined by the project. They
can be executed using [`spacy project run [name]`](https://spacy.io/api/cli#project-run)
and will run the specified commands in order. Commands are only re-run if their
inputs have changed.

| Workflow | Steps |
| --- | --- |
| `all` |  `data-to-spacy` &rarr; `train_spacy` &rarr; `evaluate` |
| `all_prodigy` | `train_prodigy` &rarr; `train_curve` |

### 🗂 Assets

The following raw assets are defined by the project.

| File | Source | Description |
| --- | --- | --- |
| `assets/raw/UC1_train_meta.jsonl` | Local | JSONL-formatted raw training data (1778 docs) |
| `assets/raw/UC1_eval_meta.jsonl` | Local | JSONL-formatted raw development data (593 docs) |

### 💯 Insights
#### Overall annotation count:

| | # Annotations | # PERSON | # EMAIL |
| --- | --- | --- |--- |
| `correct_UC01_train` | 3500 | 1011 | 272 |

#### Annotation details:

[W&B Prodigy report](https://wandb.ai/alfred-ls/Prodigy_NER/reports/Visualizing-Prodigy-UC01-datasets--VmlldzoxMDkwMzQ4)

#### Overall results:

![image](https://user-images.githubusercontent.com/52454409/137497207-aaf6a3ca-b57f-4fb9-a6ab-369729e3d85a.png)

![image](https://user-images.githubusercontent.com/52454409/137497379-42ddd39e-5f02-453e-86a2-55434afbdfa9.png)




<!-- SPACY PROJECT: AUTO-GENERATED DOCS END (do not remove) -->
