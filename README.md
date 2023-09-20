# AI-powered Data Discovery

## Objective:
Revolutionize data discoverability by integrating AWS Glue Data Catalog, Amazon Kendra, GPT-4, Amazon S3. Here's a brief overview of each component:

![image](https://github.com/suitedaces/ai-data-discovery/assets/50865782/9435d0b0-2243-4feb-8f11-88678e2a679a)

- **AWS Glue Data Catalog**: Centralized metadata repository that discovers, catalogs, and transfers datasets to Amazon S3.

- **Amazon Kendra**: ML-powered search engine that indexes data from S3, providing contextually relevant search results based on user queries.

- **OpenAI GPT-4**: Natural language processing layer that refines user queries to optimize search results from Kendra, and explain 

- **Amazon S3**: Primary data storage solution housing datasets and metadata for Kendra indexing.

- **Client-Side Web App** (Chat Interface): User interface for query input and search result display, integrated with GPT-4 and Kendra.

## Steps:
1. Data Identification:
 - Identify available datasets for relevance.
 - Collaborate with stakeholders to finalize data selection.

2. AWS Glue Data Catalog Setup:
 - Create Glue Databases and Tables for the datasets repository we find. We can configure data crawlers to automate this.
 - Transfer cataloged data to Amazon S3 using the boto3 library for AWS in Python.

3. Amazon Kendra Configuration:
 - Link Kendra to S3 as its data source. It can parse PDFs, excel, txt, csv, ppt files etc.
 - Define and schedule indexing parameters. Create an index.
 - (Optional) Fine-tune search parameters for optimal results.
 - (Optional) Add more out-of-the-box data connectors that are available (Confluence, Sharepoint, etc.) 

4. Develop client-side web app:
 - Develop a chat interface using Streamlit or React, connect it to Kendra
 - Integrate Kendra and GPT-4 - user query flow should be: client (query) --sent-to-> kendra -> client --calls-> OpenAI GPT-4 API

Let's break this down further.
