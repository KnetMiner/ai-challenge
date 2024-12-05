# ai-challenge
### We provided a Vector Database containing details about Trait Ontology terms to 3 GPT models and prompted them to extract the Gene Trait relations from various publication abstracts. The 3 models returned varying outputs, as can be seen in their respective CSVs. Some of the rows in the output files have the wrong Trait Name (trait_name) mapped to the Trait IDs (trait_id). Your task is to analyze the CSVs and solve the following -

### 1) For each row in these CSVs, come up with a correctness score metric, which tells whether the Trait Name & the Trait ID of that row are correctly mapped or not. 
Eg. of a correct mapping: 
**trait_name: abiotic stress tolerance, trait_id: TO:0000168**

Eg. of an incorrect mapping:
**trait_name: root system depth, trait_id: TO:0000343**

### 2) Rank the 3 CSVs in terms of the overall correctness of this mapping.

### 3) Given a wrong mapping, how would you go about assigning the correct Trait ID to the predicted Trait term?

### 4) Prepare a short presentation on your findings.
