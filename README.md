RAG-Based Medical Assistant
Overview
This project develops a Retrieval-Augmented Generation (RAG) AI solution to assist healthcare professionals by providing quick access to reliable medical knowledge. It addresses challenges like information overload, enabling faster decision-making, improving diagnostics, and standardizing care practices. The system leverages the Merck Manuals, a comprehensive medical reference, to answer common medical queries such as diagnostic assistance, drug information, treatment plans, specialty knowledge, and critical care protocols.
The project is implemented as a Jupyter notebook (medical1.ipynb) and uses various Python libraries to process the Merck Manuals PDF, create a knowledge base, and generate responses to medical queries.
Features

Diagnostic Assistance: Retrieve symptoms and treatments for conditions (e.g., "What are the common symptoms and treatments for pulmonary embolism?").
Drug Information: Provide trade names and details for medications (e.g., "Can you provide the trade names of medications used for treating hypertension?").
Treatment Plans: Suggest first-line and alternative treatments (e.g., "What are the first-line options for managing rheumatoid arthritis?").
Specialty Knowledge: Outline diagnostic steps for specific fields (e.g., "What are the diagnostic steps for suspected endocrine disorders?").
Critical Care Protocols: Deliver protocols for urgent scenarios (e.g., "What is the protocol for managing sepsis in a critical care unit?").

Prerequisites

Python 3.13 or higher
Git for version control
A virtual environment (recommended)

Installation

Clone the Repository:
git clone https://github.com/your-username/RAGbased_medical_assistant.git
cd RAGbased_medical_assistant


Set Up a Virtual Environment (optional but recommended):
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install Dependencies:The project requires several Python libraries. Install them using the following commands (as listed in the notebook):
pip install llama-cpp-python
pip install numpy pandas
pip install huggingface_hub tiktoken pymupdf
pip install langchain langchain-community chromadb


For GPU support with llama-cpp-python, ensure you have CUDA installed and uncomment the GPU installation command in the notebook.
Note: You may need to restart the Jupyter kernel after installing some packages, as mentioned in the notebook outputs.


Download the Merck Manuals:The project uses the Merck Manuals (a 4,000+ page PDF) as the data source. Place the PDF file (medical_diagnosis_manual.pdf) in the project directory. (Note: The PDF is not included in the repository due to licensing restrictions.)


Usage

Launch Jupyter Notebook:
jupyter notebook

Open medical1.ipynb in your browser.

Run the Notebook:

Execute the cells in order to install dependencies, process the Merck Manuals PDF, and set up the RAG system.
The notebook includes code to load the PDF, extract text, and prepare the knowledge base using langchain and chromadb.


Query the System:Once the setup is complete, you can use the system to answer medical queries. Example queries:

"What are the common symptoms and treatments for pulmonary embolism?"
"What is the protocol for managing sepsis in a critical care unit?"



Project Structure

medical1.ipynb: Main Jupyter notebook containing the RAG implementation.
medical_diagnosis_manual.pdf: The Merck Manuals PDF (not included; must be provided by the user).
chroma_sqlite3_medical_db: Directory for storing the Chroma vector database (created during execution).

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make your changes and commit (git commit -m "Add your feature").
Push to the branch (git push origin feature/your-feature).
Open a Pull Request.

License
This project is licensed under the MIT License. See the LICENSE file for details (to be added).
Acknowledgments

The Merck Manuals for providing comprehensive medical knowledge.
Libraries like langchain, chromadb, and pymupdf for enabling this project.

Contact
For questions or feedback, please reach out to Rudra Prakash (rudra.prakash@example.com).
