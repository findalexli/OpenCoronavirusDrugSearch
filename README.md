# OpenCoronavirusDrugSearch
Open-source search for approved drugs for treatment of Coronavirus 
![Image0](https://miro.medium.com/max/2800/1*uC40oYHy1rF1ZoXP0piBvw.jpeg)
## Motivation: 
Given the scale and spread of the coronavirus breakout,  there is a immediate and urgent need for medicines which does not exist for this virus yet. Besides’ Gilead’s clinical trial of their drug, BenevolentAI has recently published this article on [Lacent](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(20)30304-4/fulltext?rss=yes#articleInformation). They used their company’s own knowledge graph, curated originally from scientific literature, and identified baricitinib as a suggested potential treatment. 
![Image](https://els-jbs-prod-cdn.literatumonline.com/cms/attachment/8d2d80c6-d53e-4123-9877-5c64dda88249/gr1.jpg)

But clinical biologists are very researved about this. One obvious operational issue is that clinical studies must take place before this approved drug is repurposed for the treatment of coronavirus. But another issue is that as a private company, BenevolentAI’s database and code are not going to be open. Convincing clinical people to do clinical study about a black-box result is almost not gonna succeed. End-to-end model transparency and intepretability is needed. 

## Steps and scoping 

### Step 0: Scoping end goal

We would like to reproduce a knowledge graph to recommend approved drugs, in a completely open-source manner (GNU General Public License v3.0) including dataset, pipeline, algorithm and code. In this process, we will constantly seak feedback from clinicians and biotech professionals in order to be communicative and relevant to the Coronavius treatment.  

### Step 1. Identify the right data 
![Image 2](https://miro.medium.com/max/7012/1*kUebZxFOUjJGeWX7YoCIVg.png)

To get started to construct the complex relationships between compounds, genes, diseases an proteins, we need to identify soruces of raw data. 

Candidates: 
[Drugbank](https://www.drugbank.ca)  
[Pubtator](https://www.ncbi.nlm.nih.gov/research/pubtator)


### Steps 2. Normalizing raw data
Grakn, a open source graph database utilises the entity-relationship model to group each concept into either an entity, attribute, or relationship. This means that all we have to do is to map each concept to a schema concept type, and recognize the relationships between them. 

Reference
 https://blog.grakn.ai/drug-discovery-knowledge-graphs-46db4212777c 

### Working progress, please share your thought either by submitting a pull request or a issue. 

TODO list 
1. Curate a corpus from Pubmed abstracts(Reporting to Alex Li), identify keywords to extracting Pubmed articles (Protein mentioned in Benevelent AI's graph..., anything else? )and download the abstracts using Pubtator API (sample code is ready to be uploaded soon) 


2. Search for a compound-compound similarity database and how to ingest it (Reporting to Lan Gao)

3. For anyone looking at this page, if you see any thing missing or if you like to help, please do! You can submit pull request or raising a issue. 
