# AI Engineer Challenge: Trait Ontology Mapping

## **Background**
This challenge involves evaluating the correctness of gene-trait mappings extracted by LLM models using data stored in a Trait Ontology (TO) vector database. The goal is to assess the alignment of trait names to their corresponding TO IDs and propose a systematic approach to correct errors.

---

## **Your Tasks**
You will analyse outputs from three LLM models stored in separate CSV files. Each row contains a `trait_name` and `trait_id`. Use the accompanying `trait_ontology_details.txt` file to validate these mappings. Your submission should answer the following:

### **Task 1: Develop a Correctness Metric**
- **Goal**: Define a quantitative metric that evaluates the correctness of each row in the CSV files. 
- **Considerations**:
  - Does the `trait_name` correspond to the `trait_id` based on the `trait_ontology_details.txt`?
  - Partial matches or synonyms (if applicable).
  - Confidence in mapping correctness based on string similarity or semantic context (e.g., Levenshtein distance, embeddings).

---

### **Task 2: Rank CSVs Based on Correctness**
- **Goal**: Aggregate the correctness scores across rows and rank the 3 CSVs based on the overall quality of their mappings.
- **Deliverable**: A ranked list of the files, supported by a brief explanation of your scoring methodology.

---

### **Task 3: Propose a Method to Correct Errors**
- **Goal**: Outline a systematic approach to identify and correct mismatches.
- **Key Requirements**:
  - Use `trait_ontology_details.txt` to suggest correct `trait_id`s for mismapped terms.
  - Justify your proposed solution (e.g., by leveraging similarity measures, ontology hierarchies, or semantic embeddings).

---

### **Task 4: Predict TO Mappings for Given Trait Terms**
- **Goal**: Apply your methods to predict TO mappings for a set of challengine trait terms that don't have exact matches in TO. The aim is to provide a well structured output for a manual data curation step, helping to reduce the amount of time needed for manual review.
- **Key Requirements**:
  - Use `validation_trait_names.txt` to evaluate your model or approach.
  - Provide a confidence value for the mapping, where 0 means the trait term does not exist in TO (e.g. vernalization requirement), and 1 means the identified TO term is 100% correct (e.g. spike length -> TO:0002768 -> spikelet length).
  - Generate explanations for low-confidence predictions using an LLM.
  - Submit a CSV with columns: `trait_term, to_id, to_term, confidence, explanation` and your code.

---

## **Deliverables**
1. **Interactive Notebook**:
   - Include code, visualisations, and explanations of your approach.
   - Document key functions and decisions thoroughly.

2. **Summary Presentation**:
   - Prepare a 5-slide deck explaining:
     - Your methodology for each task.
     - Results (e.g., correctness metric, ranked CSVs, error corrections).
     - Insights or challenges encountered.
   - Use visualisations to support your findings (e.g., charts, tables).

3. **Code Documentation**:
   - Clean, well-structured code with clear comments.
   - Include instructions for running your notebook.

---

## **Evaluation Criteria**
- **Technical Proficiency**:
  - Innovative metric definition and accurate validation logic.
  - Effective error correction methodology.
- **Analytical Rigor**:
  - Sound justification for ranking and corrections.
  - Clear and interpretable visualisations.
- **Communication**:
  - Clarity in documentation and presentation.
  - Ability to explain technical concepts to a non-technical audience.

---

## **Submission**
- Submit the notebook and presentation in a compressed folder.
- Use the following structure:
  ```plaintext
  submission/
    ├── analysis_notebook.ipynb
    ├── predicted_trait_mappings.csv
    ├── presentation.pdf
    ├── README.md
