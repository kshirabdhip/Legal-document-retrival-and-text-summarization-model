# A document retrieval and summarization model for regulatory analysis.

Regulations are a form of law with some general rules made by persons to whom Parliament has delegated authority. In recent years the Canadian government has made its regulation public and discussed the problem they face in the regulations landscape. Every year regulations keep on updating, and organizations that do not comply with the government’s regulations can end up paying billions of dollars in penalties. To make themselves compliant to regulations, organizations need to spend millions to third party companies to help them follow the rules.
To solve the above problem, we are trying to come up with a model that will extract regulations with their summaries relevant to a user's interest.

## How to execute this project??

 1. To clean the data run:
 ```bash
* preprocessing.ipynb
```
2. For model training run:
```bash
* training.ipynb
```
3. For model output run:
```bash
Inference_model.ipynb
```

### Model Architecture:

<div align="center">
<img src="https://github.com/kshirabdhip/Data-Science---MRP/blob/master/model_architecture.png" width="400" height="500">
</div>

## Results:
 - Input the document database the query words and number of similar documents to retrieve:
   example "flight security", 2
 - Outputs are the relevent document's title and summaries. It extracts the documents if you set content = True in inference.ipynb file.
 
 #### Set following code in Inference_model.ipynb

```python
query_string =  "airport security"
number_of_doc = 4
tf_idf = tf_doc_df

test_doc = query_and_op( query_string, number_of_doc, tf_doc_df )
doc_to_query = query_documents
similarity_indx = test_doc
title = True
content = False
summary = True
test_rank = True

extract_summary(doc_to_query,similarity_indx, title,content,summary,test_rank)

```
 
 
 <div align="left">
<img src="https://github.com/kshirabdhip/Data-Science---MRP/blob/master/result.JPG" width="800" height="300">
</div>
 

#### To know the project in detail please read the "Kshirabdhi_Patel_MRP_Report_MSc_Data Science and Analytics.pdf" file.
