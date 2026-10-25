# French Hypersense Classification with ICL and QLoRA

Course project for **Current Topics in NLP and Society**, Université Paris Cité.

**Authors:** Peng CHEN and Yiwei ZUO

We classify French Wiktionary word senses into 12 hypersense categories using their definitions, with or without the lemma. We compare two approaches using the 4-bit instruction-tuned model `unsloth/Qwen3-4B-Instruct-2507-bnb-4bit`:

- **In-context learning (ICL):** compare demonstration counts and lemma inclusion, with an additional comparison of label-code generation and log-probability scoring.
- **QLoRA:** compare lemma inclusion and LoRA adaptation of Attention + FFN versus Attention only.

Configurations are compared on `rand-dev`; final results for the selected methods are reported on `rand-test` and `freq-test`. All `protect-frsemcor` instances are excluded. The Attention-only experiment is a supplementary development-set comparison.

## Report and Code

- [Report and experiment notebook on GitHub](https://github.com/Yiwei-ZUO/french-hypersense-classification-with-ICL-and-QLoRA)
- [Shared Google Drive folder](https://drive.google.com/drive/folders/1lErw7KFkmEcxeb6VT7tXk_EoHaX0PNJX)

The notebook includes saved outputs for inspection. Its default results-only mode also requires prediction CSVs and training logs that are not included in this repository. To rerun the experiments, configure the data and output paths and enable the relevant training or inference switches in a GPU environment.
