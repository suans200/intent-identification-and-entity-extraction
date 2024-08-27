# Intent Identification and Entity Extraction
# Researcher
References: https://aclanthology.org/2023.findings-eacl.140.pdf
Following are the details of various files and the models they are using :-

------------------- Intent Recognition --------------------

Initial Dataset setup logic is same in almost all the files. So, some initial codes of these files are almost same. For details, please visit the code.

ir_svm_en.ipynb : English, TF-IDF Vectorization, SVM

ir_rob_en.ipynb : English, "roberta-base" as model checkpoint


------------------- Entity Extraction --------------------

For entity extraction, matching of below tags were done through fuzzywuzzy library's threshold string matching by calculating a fuzzy ratio:

label__ = {
    'O': 0,
    'B-treatment': 1,
    'I-treatment': 2,
    'B-disease': 3,
    'I-disease': 4,
    'B-drug': 5,
    'I-drug': 6
}
Initial Dataset setup logic is same in almost all the files. So, some initial codes of these files are almost same. For details, please visit the code.

ee_svm_en.ipynb : English, TF-IDF Vectorization, SVM

ee_rob_en.ipynb : English, "roberta-base" as model checkpoint

ee_xlmr_hi.ipynb : Hindi, "xlm-roberta-base" as model checkpoint

ee_dtrans_hi.ipynb : Hindi, GoogleTranslator(Hindi to English), "emilyalsentzer/Bio_ClinicalBERT" as model checkpoint

ee_bridge_hi.ipynb : Bengali, GoogleTranslator(Bengali to Hindi), GoogleTranslator(Hindi to English), "emilyalsentzer/Bio_ClinicalBERT" as model checkpoint
