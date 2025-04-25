In this Kaggle competition you are tasked with coming up with a modified BERT
architecture with the highest test accuracy on a held-out portion of a text classification
dataset called “AGNEWS”, under the constraint that your model has no more than 1
million trainable parameters.
You will start with a specific version of BERT (called RoBERTa). The only type of
modification you are allowed to make to BERT is low-rank adaptation [LoRA]. See
here or here for an explanation of what LoRA is; the high level idea is that each (frozen)
weight matrix in BERT is perturbed by a trainable low-rank matrix, where you can set
the rank and the strength of the perturbation. More details are below, and there is also
a demo notebook posted on the Kaggle competition site, which uses a popular LLM
fine-tuning library called BitsAndBytes.
