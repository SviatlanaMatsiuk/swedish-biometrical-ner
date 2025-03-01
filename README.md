# Group Project CM2011 - Named Entity Recognition (NER) and Entity Linking

## Local installation
conda install pytorch==2.0.1 cpuonly -c pytorch
conda install --file requirements.txt  -c conda-forge

## Introduction
Textual data, which comprised a major portion of the internet, is a veritable treasure trove of information. The rise of LLMs has also brought a lot of attention to this form of data, and its many uses. However, despite the power of LLMs, mining free text for relevant information remains a challenge, and good datasets for medical applications in languages other than English are few and far between. The only way to extract domain specific (medicine/law) information from free text is to either create a dataset and train a domain specific model, or take a base model and fine-tune it for domain and task specific goals. While using this extracted/structured information in downstream tasks can be accomplished, creating good medical datasets, and structuring this information for use by clinicians is accomplished by linking parts of text (such as entities) to medical ontologies, such as ICD, ICF, LOINC etc. This ensures that unstructured information gets structures in the long run. 

## Aim
Your task in this group project is to choose and fine-tune an LLM for Swedish Biomedical Named Entity Recognition. There are no openly published models that can accomplish the extraction of information from biomedical texts (for example, clinician notes in electronic health records). The only open dataset for Swedish Biomedical NER is: https://huggingface.co/datasets/community-datasets/swedish_medical_nerLinks to an external site.

## Tasks
1. Conduct a small survey of LLMs for NER in Swedish. Structure the survey based on performance, relevance to the project aim, and any other metrics and dimensions you think is relevant to accomplish this task. Note that two approaches are possible, fine-tuning a Swedish LLM, or translating the dataset into English, and further fine-tuning a biomedical model for NER and other tasks (for example BioBERTLinks to an external site.). Think critically about the advantages and disadvantages of both approaches.
2. Make a choice of model to fine-tune from the survey, and motivate your choice.
3. Fine-tune the model using the dataset linked above. You can use HuggingFace transformers library, and tutorials to accomplish this. Extract entities from the dataset.
4. Link the entities to concepts in medical ontologies, such as ICD/ICF/Loinc/Rx. You might need to train a different model to link extracted entities /text with concepts from the ontologies. You can download the ontology files here: https://www.socialstyrelsen.se/statistik-och-data/klassifikationer-och-koder/kodtextfiler/ Links to an external site. Create a strategy to accomplish this, for example:
a. A simple search through ontologies
b. ML based on classifying entities with data from ontologies.
c. Fine-tuning the chosen model with text from the ontologies.
5. Report the accuracy or other metrics and explainability (attention weights/SHAP/Other as relevant).
6. Perform a simple external validation, for example by choosing errors (you can identify these by model scores, low confidence), for both tasks 3 and 4 and reason as to why and where the model might be going wrong. 


