Fusion–Hybrid Recommender System using GRU, GAT, and Product Feature Encoding

This repository contains the complete workflow for building a Hybrid Recommender System for E-Commerce that integrates:

GRU — models user purchase sequences

Graph Attention Networks (GAT) — captures product–product relationships

TF–IDF Feature Encoding — learns product meaning from metadata

The project was developed and evaluated on the Amazon All-Beauty dataset.
The system evolves across three notebook versions — with the Final Model achieving the best performance (~98% Recall@10).

📂 Repository Files
1️⃣ RS_Project_BAseline.ipynb — Baseline Model

Model Type: GRU + GAT (Score-Level Hybrid)

GRU learns sequential user behaviour

GAT learns product graph relations

The two outputs are combined only at inference

This model works well but does NOT fuse representations during training.

Performance: ~78% Recall@10

2️⃣ First_model.ipynb — Feature-Enhanced Model

Model Type: GRU + GAT + Metadata (Partially Integrated)

Adds TF–IDF metadata features

Begins hybrid integration

Still not fully fused at representation level

Performance: Improved over baseline

3️⃣ Final_model.ipynb — ⭐ Fusion–Hybrid Model (Best Model)

Model Type: End-to-End Representation-Level Fusion

This is the final and best-performing model.
It jointly learns:

✅ GRU user-sequence embeddings

✅ GAT product-graph embeddings

✅ TF–IDF metadata embeddings

All embeddings are fused into a single latent representation during training, enabling stronger learning and better recommendations.

✅ Final Model Performance
Metric	Value
Recall@10	⭐ ≈ 97.94% (~98%)
Hit Rate@10	97.94%
NDCG@10	0.9518
MRR	0.9428

🔥 This is a major improvement over the baseline (~78% Recall@10).

📊 Dataset Summary

Source: Amazon All-Beauty Reviews + Metadata

After 5-core filtering:

961 users

49 products

5084 interactions

🧠 Recommendation Modes Supported

Personalized user-based recommendations

Graph-based similar item suggestions

Metadata-based similarity search

Hybrid blended recommendations

Category-aware smart filtering

🏗 Technologies Used

Python

PyTorch & PyTorch Geometric

Scikit-Learn

Pandas / NumPy

Matplotlib

▶️ How to Run

Recommended notebook order:

RS_Project_BAseline.ipynb

First_model.ipynb

Final_model.ipynb ← best model

Running the notebooks will:

✔ preprocess the dataset
✔ train the models
✔ evaluate ranking metrics
✔ generate recommendations

🧊 Cold-Start Handling

New users → graph + metadata recommendations

New items → metadata encoder support

📌 Final Comparison
Notebook	Model Type	Fusion Type	Metadata Used	Recall@10
RS_Project_BAseline	GRU + GAT	Score-Level	No	~78%
First_model	GRU + GAT	Partial	Yes	Higher
Final_model	GRU + GAT + Metadata	Representation-Level	Yes	~98%
