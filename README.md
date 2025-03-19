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

python
Copy
Edit
import spacy
nlp = spacy.load("en_core_web_sm")
text = "Elon Musk founded SpaceX in 2002 and Tesla in 2003."
doc = nlp(text)
for ent in doc.ents:
    print(ent.text, "→", ent.label_)



 2. Dependency Parsing
Dependency Parsing dengan spaCy

python
Copy
Edit
import spacy
nlp = spacy.load("en_core_web_sm")
text = "Elon Musk founded SpaceX in 2002 and Tesla in 2003."
doc = nlp(text)
for token in doc:
    print(token.text, "→", token.dep_, "(head:", token.head.text, ")")


🔹 3. POS Tagging
POS Tagging dengan spaCy

python
Copy
Edit
import spacy
nlp = spacy.load("id_core_news_sm")
text = "Saya sedang membaca buku di perpustakaan."
doc = nlp(text)
for token in doc:
    print(f"{token.text} → {token.pos_}")



POS Tagging dengan NLTK

python
Copy
Edit
import nltk
from nltk.tokenize import word_tokenize
from nltk.tag import pos_tag
nltk.download("punkt")
nltk.download("averaged_perceptron_tagger")
text = "Saya membeli buku yang sangat bagus di toko itu."
tokens = word_tokenize(text)
pos_tags = pos_tag(tokens)
print(pos_tags)




🎯 Hasil & Analisis
NER: Model bisa mengenali entitas seperti nama orang, organisasi, dan tempat, namun terkadang terjadi kesalahan tanpa konteks yang kuat.
Dependency Parsing: Analisis hubungan antar kata membantu memahami struktur kalimat.
POS Tagging: POS Tagging berguna untuk memahami peran kata dalam kalimat dan penting dalam NLP tasks lainnya.




