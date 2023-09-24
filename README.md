
# QA with LLM and RAG (Retrieval Augumented Generation)

This project is a Question Answering application with Large Language Models (LLMs) and Amazon Kendra. An application using the RAG(Retrieval Augmented Generation) approach retrieves information most relevant to the user’s request from the enterprise knowledge base or content, bundles it as context along with the user’s request as a prompt, and then sends it to the LLM to get a GenAI response.

LLMs have limitations around the maximum word count for the input prompt, therefore choosing the right passages among thousands or millions of documents in the enterprise, has a direct impact on the LLM’s accuracy.

In this project, Amazon Kendra is used for knowledge base.

The overall architecture is like this:

![rag_with_kendra_arch](https://d2908q01vomqb2.cloudfront.net/f1f836cb4ea6efb2a0b1b99f41ad8b103eff4b59/2023/05/02/ML-13807-image001-new.png)

### Overall Workflow

1. Deploy the cdk stacks (For more information, see [here](./cdk_stacks/README.md)).
  - An Amazon Kendra for knowledge base.
  - A SageMaker Endpoint for text generation.
2. Open SageMaker Studio and then open a new terminal.
3. Run the following commands on the terminal to clone the code repository for this project:
   ```
   git clone https://github.com/ksmin23/rag-with-amazon-kendra.git
   ```
4. Run Streamlit application. (For more information, see [here](./app/README.md))

### References

  * [Quickly build high-accuracy Generative AI applications on enterprise data using Amazon Kendra, LangChain, and large language models (2023-05-03)](https://aws.amazon.com/blogs/machine-learning/quickly-build-high-accuracy-generative-ai-applications-on-enterprise-data-using-amazon-kendra-langchain-and-large-language-models/)
  * [(github) Amazon Kendra Retriver Samples](https://github.com/aws-samples/amazon-kendra-langchain-extensions/tree/main/kendra_retriever_samples)
  * [Build a powerful question answering bot with Amazon SageMaker, Amazon OpenSearch Service, Streamlit, and LangChain (2023-05-25)](https://aws.amazon.com/blogs/machine-learning/build-a-powerful-question-answering-bot-with-amazon-sagemaker-amazon-opensearch-service-streamlit-and-langchain/)
  * [Build Streamlit apps in Amazon SageMaker Studio (2023-04-11)](https://aws.amazon.com/blogs/machine-learning/build-streamlit-apps-in-amazon-sagemaker-studio/)
  * [Question answering using Retrieval Augmented Generation with foundation models in Amazon SageMaker JumpStart (2023-05-02)](https://aws.amazon.com/blogs/machine-learning/question-answering-using-retrieval-augmented-generation-with-foundation-models-in-amazon-sagemaker-jumpstart/)
  * [Amazon OpenSearch Service’s vector database capabilities explained](https://aws.amazon.com/blogs/big-data/amazon-opensearch-services-vector-database-capabilities-explained/)
  * [LangChain](https://python.langchain.com/docs/get_started/introduction.html) - A framework for developing applications powered by language models.
  * [Streamlit](https://streamlit.io/) - A faster way to build and share data apps
  * [Improve search relevance with ML in Amazon OpenSearch Service Workshop](https://catalog.workshops.aws/semantic-search/en-US) - Module 7. Retrieval Augmented Generation
  * [rag-with-amazon-opensearch](https://github.com/ksmin23/rag-with-amazon-opensearch) - Question Answering application with Large Language Models (LLMs) and Amazon OpenSearch Service
  * [rag-with-postgresql-pgvector](https://github.com/ksmin23/rag-with-postgresql-pgvector) - Question Answering application with Large Language Models (LLMs) and Amazon Aurora Postgresql