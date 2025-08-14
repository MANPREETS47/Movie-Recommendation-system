# 🎬 Movie Recommendation System

An AI-powered **content-based movie recommendation system** built using **TensorFlow Functional API**, trained on real-world **Netflix dataset**.  
The system analyzes **content features** like movie ID, language, and type to recommend similar content to users.

---

## 📌 Features
- Works with **real Netflix content dataset**
- **Content-based filtering** using embeddings for:
  - Content ID
  - Language ID
  - Content Type
- Built using **TensorFlow Functional API**
- **Self-supervised training** (predicting content from its own features)
- Retrieves **Top-K similar content** for any given movie/show
- Deployment-ready for web applications

---

## 🛠️ Tech Stack
- **Python 3**
- **TensorFlow / Keras** (Functional API)
- **NumPy, Pandas** for preprocessing
- **Matplotlib / Seaborn** for visualization
- **Jupyter Notebook** for development

---

## 📂 Dataset
The dataset contains:
- `Content_ID`: Unique identifier for each movie/show
- `Title`: Name of the content
- `Language_ID`: Language indicator
- `ContentType_ID`: Indicates if it's a Movie or TV Show
- `Hours Viewed`: Popularity metric

**Preprocessing:**
- Removed missing values
- Converted categorical data into numerical IDs
- Prepared features for embedding layers

---

## ⚙️ Model Architecture
1. **Inputs**:
   - `content_id` (shape: `(1,)`)
   - `language_id` (shape: `(1,)`)
   - `type_input` (shape: `(1,)`)
2. **Embedding Layers** for each feature
3. **Flatten Layers** to convert embeddings into vectors
4. **Concatenation Layer** to combine all vectors
5. **Dense Layers**:
   - 64 neurons (ReLU)
   - 32 neurons (ReLU)
6. **Output Layer**:
   - Softmax over all content IDs

---

## 📜 Example Usage
```python
recommend_similar("Wednesday", top_k=5)
