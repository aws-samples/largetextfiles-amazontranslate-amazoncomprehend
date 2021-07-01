# A sentence tokenizer as input to Amazon Translate and AWS Comprehend - in 5000 byte files ![image](https://user-images.githubusercontent.com/79527811/124118134-e64a1200-da68-11eb-9d36-341a7032fc95.png)


This is the code for tokenizing the large paragraphs into sentence.This helps for the case when you want to feed that sentence of the 5000 bytes size chunks to the translate or comprehend services. As attached in the code this notbook also helps for having the KMS encrypted data taken from the S3 add the transformation like IO byte based tokenization and creating a chunks of 5000 bytes file using LIFO kind of algorithm.

## Create a new repository from this template


---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, following scripts are present :

### `split_df4`

This is the function for the splitting the dataframe to the chunks of 5000 bytes this has implmented LIFO by cutting out the last sentence and rechking the size of the data frame size it to the 5000 bytes, it starts with calculating the number of the chunks requried it has been build with tolerance of 500 bytes sentence being the longest sentence possible for chunking.

### `write_file`

This is the function for writing the chunked files to KMS encrypted S3 storage.



---

## License

This library and the stack file are licensed under the MIT-0 License. See the LICENSE file.
