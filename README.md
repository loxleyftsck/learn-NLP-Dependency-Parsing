Repository ini berisi implementasi Named Entity Recognition (NER), Dependency Parsing, dan POS Tagging menggunakan berbagai pustaka NLP dalam Python.

📖 Teknologi yang Digunakan
✅ spaCy - Untuk NER, Dependency Parsing, dan POS Tagging
✅ Hugging Face Transformers - Untuk NER dengan model IndoBERT
✅ Stanza - Untuk Dependency Parsing dalam bahasa Indonesia
✅ NLTK - Untuk POS Tagging


pip install spacy transformers datasets stanza nltk
python -m spacy download en_core_web_sm
python -m spacy download id_core_news_sm

📝 Implementasi
🔹 1. Named Entity Recognition (NER)
NER dengan spaCy

🔹 2. Dependency Parsing
Dependency Parsing dengan spaCy

🔹 3. POS Tagging
POS Tagging dengan spaCy


🎯 Hasil & Analisis
NER: Model bisa mengenali entitas seperti nama orang, organisasi, dan tempat, namun terkadang terjadi kesalahan tanpa konteks yang kuat.
Dependency Parsing: Analisis hubungan antar kata membantu memahami struktur kalimat.
POS Tagging: POS Tagging berguna untuk memahami peran kata dalam kalimat dan penting dalam NLP tasks lainnya.




