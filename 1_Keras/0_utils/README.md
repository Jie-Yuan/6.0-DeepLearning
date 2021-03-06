[<h1 align = "center">:rocket: KERAS API :facepunch:</h1>][0]

---
### `import keras.preprocessing.text as T`
- `T.maketrans`
```python
'aabbcc'.translate(T.maketrans('abc', '123'))
'cba'.translate(str.maketrans("abc", "123"))
```
- `T.one_hot`: `one_hot('some thing to eat', 10) # [7, 9, 6, 4]`
- `T.text_to_word_sequence`
- `T.Tokenizer`
  ```python
  text1='some thing to eat'
  text2='some thing to drink'
  texts=[text1,text2]
  tokenizer = T.Tokenizer(10**6)
  tokenizer.fit_on_texts(texts)
  
  tokenizer.word_counts
  tokenizer.word_docs
  tokenizer.word_index
  tokenizer.index_docs
  
  tokenizer.texts_to_matrix(texts, mode='binary') # mode: one of "binary", "count", "tfidf", "freq".
  tokenizer.texts_to_sequences(texts) # tokenizer.texts_to_sequences_generator(texts)
  """
  tokenizer.fit_on_sequences([text1])
  tokenizer.sequences_to_matrix([[1, 2, 3]])
  """
  ```
---
### `import keras.preprocessing.sequence as S`
- `S.pad_sequences`
- `S.skipgrams`
- `S.make_sampling_table`

---
[0]: https://blog.csdn.net/luanpeng825485697/article/details/79137208
