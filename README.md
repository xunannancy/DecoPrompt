# DecoPrompt
Code for paper DecoPrompt : Decoding Prompts Reduces Hallucinations when Large Language Models Meet False Premises
### Dataset
As described in Section 5, we evaluate on two datasets, one from the fictitious and the other from the real world. You can find examples
Q1~Q4 on page 5 and 6.
1. **_Fictitious_**: in `./datasets/fictitious/data/jsonl`, we use 10 templates to ask more information about one description.
2. **_Authorship_**:
   1. in `./datasets/authorship/author_data.jsonl`, we provide book title and their true author pairs and ask LLMs about the author of each book. 
   2. If the model can correctly answer the question, we then substitute the true author with some celebrity (i.e., _false-premise_ in question) and ask LLMs to provide more information.
      You can find different descriptions about celebrities in `./datasets/authorship/celebrity_data.json` as the context information.