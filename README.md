### <ins>Overview</ins>

Could you circumvent the recruiter screen portion of an interview process?\
Looks like the answer is yes. \
\
\
Enter Ariana AI bot. This bot will ask your candidates basic first round of interview questions. All you need is your Open AI API key and the job description.
The bot uses Retrieval Augmented Generation (RAG) process in the following steps.

1. Using job description, retrieve job location, job title and company for which this job is posted.
2. Using the above information as metadata, insert these inputs into chat templates.
3. Ask the user/candidate basic set of interview questions & save the input to be forwarded to the hiring manager.

### <ins>Dependencies</ins>

1. Langchain
2. Chroma DB vector store
3. Streamlit app for frontend (This can be interchanged with any other frontend framework)

The dependencies can be installed through python via the command

```
pip install -r ./core/requirements. txt
```

### <ins>Retrieval Augmented Generation(RAG) process explained</ins>

The system will leverage OpenAI's language models, Python programming, and Chroma DB to break down job descriptions into smaller, manageable documents. These documents will be stored in Chroma DB, a high-performance vector database designed for efficient similarity search and retrieval.
Once the job description documents are stored in Chroma DB, the system will utilize the RAG (Retrieval-Augmented Generation) technique to query specific pieces of information from the documents.
The metadata retrieved from these documents are
* Job location
* Job title
* Name of company


The RAG technique combines the power of retrieval systems (like Chroma DB) with generative language models (like OpenAI's GPT models) to provide accurate and relevant responses to user queries.


### <ins>How to run</ins>

1. Make sure all the dependencies are installed first.
2. Run the following piece of code

```
streamlit run ./core/main.py
```
