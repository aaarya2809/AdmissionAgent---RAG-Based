
# 🎓 Admission Agent – RAG-Based AI (IBM Cloud)

This project implements a **Retrieval-Augmented Generation (RAG)**-based AI assistant to simplify the **college admission process** using IBM Watsonx, Object Storage, and vector databases.

The agent helps students:
- Retrieve eligibility criteria, fee structure, important dates, and application processes
- Ask natural language queries and get instant, accurate responses
- Select courses and understand admission policies more easily

---

## 🚀 Technologies Used

- **IBM Watsonx.ai** – Agent Lab + Prompt Lab for generative AI
- **IBM Cloud Object Storage** – Storing source documents (PDF, TXT, DOCX, etc.)
- **Watsonx Data** / **Milvus** / **Elasticsearch** – For vector storage
- **Python (Optional)** – To prepare and upload data
- **RAG (Retrieval-Augmented Generation)** – for answering queries

---

## 📁 Folder Structure

```
College-Admission-Agent/
│
├── docs/
│   ├── eligibility_criteria.txt
│   ├── fee_structure.txt
│   ├── how_to_apply.txt
│   └── important_dates.txt
│
├── notebook/
│   └── create_admission_documents.ipynb
│
├── agent_config/
│   └── vector_index_settings.json
│
└── README.md
```

---

## 🧾 Steps to Run the Agent on IBM Cloud

### 🔹 1. Set up IBM Cloud
- Log into [IBM Cloud](https://cloud.ibm.com)
- Enable your **Lite Plan** for Watsonx
- Launch **Watsonx.ai**

### 🔹 2. Prepare Documents
- Use the provided `create_admission_documents.ipynb` to generate `.txt` files
- Files include:
  - `eligibility_criteria.txt`
  - `fee_structure.txt`
  - `how_to_apply.txt`
  - `important_dates.txt`

### 🔹 3. Upload to Watsonx Agent Lab
1. Open **Watsonx → Projects → Agent Lab**
2. Click **New Agent**
3. Choose **Ground gen AI with vectorized documents**
4. In “Add files”:
   - Upload the `.txt` files created from the notebook
5. Define vector index name and purpose (e.g., `admission_info_vector`)
6. Choose **In-memory** or connect to **Milvus / Elasticsearch**

### 🔹 4. Configure Prompt
- Use a simple prompt like:
```
Answer based on the documents uploaded. Be concise and helpful.
```

### 🔹 5. Test and Deploy
- Ask natural questions like:
  - “What is the fee for MBA?”
  - “When does admission start?”
  - “How to apply for B.Tech?”
- Click **Deploy → Web App / API**

---

## 🔍 Example Questions

- ✅ *“What is the last date for admission?”*
- ✅ *“Are scholarships available for SC/ST?”*
- ✅ *“What is the eligibility for M.Tech?”*

---

## 📌 Notes

- File size limits:
  - PDF: 50MB
  - DOCX: 50MB
  - TXT: 5MB
- IBM Lite plans have usage restrictions
- Real-time update possible by modifying vector index

---

## 🙋‍♂️ Author

**Aarya Malghe**  
Project under [SB4Academia Challenge 2025]  
MIT Academy of Engineering, India

---

## 📄 License

This project is for educational use only. Contact the author for any reuse or deployment purposes.
