# Wiki Movie Plots Dataset (splitted into chunks)
Original dataset can be found [kaggle](https://www.kaggle.com/datasets/jrobischon/wikipedia-movie-plots).


The original `pandas.DataFrame` was converted to a HuggingFace `datasets.Dataset`. The dataset is splitted into chungs with a maximal size of 256 characters. Afterwards the chunks processed and converted into vector embeddings. 

```
In [1]:  ds
----------------------------------------------------------------
Out [1]: Dataset({
            features: ['text_batch', 'ref_id', 'embeddings'],
            num_rows: 372606
        })
```

For the embeddings the `sentence-transformers/all-mpnet-base-v2` sentence transformer from [huggingface](https://huggingface.co/sentence-transformers/all-mpnet-base-v2) was used.