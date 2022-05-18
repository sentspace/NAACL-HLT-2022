# SentSpace at NAACL-HLT-2022

Code accompanying the system demonstration results for NAACL-HLT 2022 SentSpace submission.
We provide an example of how SentSpace can be used to compare and visualize sets of sentences to one another using features from the _Lexical_ and _Contextual_ modules of Sentspace.

For this example demonstration, we compare two sets of materials: Human-generated text versus GPT2-XL-generated text. The texts consisted of 52 unique paragraphs {written by multiple human writers}. 
The first 10 words of each paragraph were used as a prompt to a pretrained GPT2-XL autoregressive language model (thanks to [HuggingFace Transformers](https://huggingface.co/docs/transformers/index); Wolf et al., 2020). Prompt completions were extracted across multiple random seeds using top-p sampling. We selected 5 completions per prompt that most closely matched the human-generated prompt in word length (within $\pm5$ words) to control for any length-driven correlations. As a result, we had one human-generated and 5 GPT2-XL-generated paragraphs per prompt, 
yielding a total of n=52 human-generated paragraphs and n=260 GPT2-XL-generated paragraphs.

The directory `in/` contains the input files used for analyses. These contain two CSV files, one called `CR_gpt-generated.csv` (written by GPT2-XL), and the other, `gpt2stories_sents_target1.csv` (written by humans).

The directory `out/` consists of SentSpace-produced output that is used in the notebook in this repository.
