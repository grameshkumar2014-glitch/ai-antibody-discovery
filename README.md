# ai-antibody-discovery
AI-Driven Antibody Discovery Engine
End-to-End Bioinformatics + AI Pipeline | Automated | Dashboard Enabled

<img width="1402" height="1122" alt="dashboard" src="https://github.com/user-attachments/assets/515fb2d0-fb97-4040-88fd-2e14b2a7bc09" />
Overview

This project implements a complete pipeline for antibody sequence analysis and candidate ranking using bioinformatics feature extraction and AI-based scoring.
It simulates real-world workflows used in antibody drug discovery, enabling identification of high-potential therapeutic candidates.

Input Data (Antibody Sequences)

The pipeline processes antibody variable region sequences along with frequency:

sequence,frequency
EVQLVESGGGLVQPGGSLRLSCAASGFTFSSYAMSWVRQAPGKGLEWVSAISGSGGSTYYADSVKGRFTISRDNSKNTLYLQMNSLRAEDTAVYYCARGGY,5000
QVQLVQSGAEVKKPGASVKVSCKASGYTFTNYGMNWVRQAPGQGLEWMGWINTYTGEPTYAADFKGRFAFSLETSASTAYLQINNLKNEDTATYFCAR,3000
EVQLVESGGGLVQPGGSLRLSCAASGFTFSSYAMSWVRQAPGKGLEWVSAISGSGGSTYYADSVKGRFTISRDNSKNTLYLQMNSLRAEDTAVYYCAR,1500

Each sequence represents a potential antibody candidate with its observed frequency.

Pipeline Workflow

Sequence Input
 → Feature Extraction (Biopython)
 → AI Scoring Model
 → Candidate Ranking
 → Visualization
 → Streamlit Dashboard
Features Extracted
Sequence length
Instability index (stability indicator)
Hydrophobicity (GRAVY score)
CDR region length (binding region approximation)

AI Scoring Strategy

Candidates are ranked using a multi-factor scoring system:

Frequency (clonal expansion signal)
Stability (instability index)
Physicochemical properties
CDR region characteristics

Automated Execution

Run the complete pipeline with one command:

./run_pipeline.sh

This executes:

Feature extraction
AI scoring
Candidate ranking
Plot generation
Dashboard launch

Manual Execution (Optional)
python scripts/features.py
python scripts/scoring.py
python scripts/plot.py
streamlit run app/dashboard.py

Output
results/features.csv → Extracted features
results/ranked_candidates.csv → Ranked antibody candidates
results/plot.png → Score visualization
Interactive dashboard (Streamlit)

Dashboard Preview

Tech Stack
Python
Pandas, Biopython
Scikit-learn
Matplotlib
Streamlit
Docker

Docker Support
docker build -t antibody-engine .
docker run -p 8501:8501 antibody-engine

Key Insight

This pipeline demonstrates how biological sequence data can be transformed into actionable insights using computational modeling and AI-based ranking.

Why This Project Matters

This project showcases:

Bioinformatics pipeline development
AI-driven decision systems
Automation and reproducibility
End-to-end system design
Real-world drug discovery workflow simulation

Author

Dr. Ramesh Kumar Gopal, PhD.,

Positioning Statement

Developed an automated AI-driven antibody discovery pipeline integrating bioinformatics feature extraction, computational scoring, and interactive visualization.
