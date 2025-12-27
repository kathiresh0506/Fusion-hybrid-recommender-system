# Fusion-hybrid-recommender-system
Fusion–Hybrid Recommender System using GRU, GAT, and Product Feature Encoding

This repository contains the complete workflow for building a Hybrid Recommender System for E-Commerce that integrates:

GRU — models user purchase sequences

Graph Attention Networks (GAT) — captures product–product relationships

TF–IDF Feature Encoding — learns product meaning from metadata

The project was developed and evaluated on the Amazon All-Beauty dataset.
The model evolves across three notebook versions — with the Final Model giving the best performance (~98% Recall@10).

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

Still not fully representation-level fused

Performance: Improved over baseline

3️⃣ Final_model.ipynb — ⭐ Fusion–Hybrid Model (Best Model)

Model Type: End-to-End Representation-Level Fusion

This is the best and final version.

It jointly learns:

✔ GRU user-sequence embeddings
✔ GAT product-graph embeddings
✔ TF–IDF metadata embeddings

and fuses them into a single latent representation during training.

✅ Final Model Performance
Metric	Value
Recall@10	⭐ ≈ 97.94% (~98%)
Hit Rate@10	97.94%
NDCG@10	0.9518
MRR	0.9428
🔥 This is a major improvement over the baseline (~78% Recall@10)
📊 Dataset Summary

Amazon All-Beauty Reviews + Metadata

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

Recommended order:

RS_Project_BAseline.ipynb

First_model.ipynb

Final_model.ipynb ← best model

Running the notebooks:

✔ preprocesses the dataset
✔ trains the models
✔ evaluates ranking metrics
✔ generates recommendations

🧊 Cold-Start Handling

New users → graph + metadata recommendations

New items → metadata encoder support

📌 Final Comparison
Notebook	Model Type	Fusion Type	Metadata Used	Recall@10
RS_Project_BAseline	GRU + GAT	Score-Level	No	~78%
First_model	GRU + GAT	Partial	Yes	Higher
Final_model	GRU + GAT + Metadata	Representation-Level	Yes	~98%
👥 Authors

Team 9
Department of Artificial Intelligence & Data Science
PSG Institute of Technology and Applied Research

📜 Purpose

This project is intended for academic and research use.

If you want, I can also:

🔹 shorten this
🔹 make it more formal
🔹 or rewrite for resume/interview use

Just tell me 🙂

i just want to paste this content

Perfect 👍 — here is the final clean README.md ONLY.
You can copy–paste directly into GitHub — no edits needed.

Fusion–Hybrid Recommender System using GRU, GAT, and Product Feature Encoding

This repository contains the complete workflow for building a Hybrid Recommender System for E-Commerce that integrates:

GRU — models user purchase sequences

Graph Attention Networks (GAT) — captures product–product relationships

TF–IDF Feature Encoding — learns product meaning from metadata

The project was developed and evaluated on the Amazon All-Beauty dataset. The system evolves across three notebook versions — with the Final Model achieving the highest performance (~98% Recall@10).

📂 Repository Files
1️⃣ RS_Project_BAseline.ipynb — Baseline Model

Model Type: GRU + GAT (Score-Level Hybrid)

GRU learns sequential user behaviour

GAT learns product–product graph structure

Outputs are combined only at inference time

This model performs well, but does not fuse representations during training.

Performance: ~78% Recall@10

2️⃣ First_model.ipynb — Feature-Enhanced Model

Model Type: GRU + GAT + Metadata (Partially Integrated)

Adds TF–IDF metadata features

Begins hybrid integration

Still not fully fused at representation level

Performance: Improved compared to baseline

3️⃣ Final_model.ipynb — ⭐ Fusion–Hybrid Model (Best Model)

Model Type: End-to-End Representation-Level Fusion

This is the final and best-performing model.

It jointly learns:

GRU-based user sequence embeddings

GAT-based item graph embeddings

TF–IDF-based metadata embeddings

All embeddings are fused into a single representation during training, enabling stronger learning and better recommendations.

✅ Final Model Performance
Metric	Value
Recall@10	⭐ ≈ 97.94% (~98%)
Hit Rate@10	97.94%
NDCG@10	0.9518
MRR	0.9428

This is a major improvement over the baseline (~78% Recall@10).

📊 Dataset Summary

Amazon All-Beauty Reviews + Metadata

After 5-core filtering:

961 users

49 products

5084 interactions

🏗 Technologies Used

Python

PyTorch & PyTorch Geometric

Scikit-Learn

Pandas / NumPy

Matplotlib

📌 Final Comparison Summary
Notebook	Model Type	Fusion Type	Metadata Used	Recall@10
RS_Project_BAseline	GRU + GAT	Score-Level	No	~78%
First_model	GRU + GAT	Partial	Yes	Higher
Final_model	GRU + GAT + Metadata	Representation-Level	Yes	~98%
