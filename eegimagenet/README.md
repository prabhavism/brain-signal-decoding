# EEG-ImageNet track

Dataset: EEG-ImageNet (2024 release, Hugging Face: PromiseZ5Q2SQ/EEG-ImageNet).
Used file 1 only (8 participants), 62 channels.

Pipeline (eegimagenet_pipeline.ipynb):
- band-pass 1 to 40 Hz, downsample 1000 -> 128 Hz
- drop extreme-amplitude epochs, z-score per channel within each participant
- 434 features per epoch: log band power (delta, theta, alpha, beta, gamma), variance, line length
- models: LinearSVC, LDA, Random Forest
- evaluation: within-participant 5-fold and LOSO

Features are not in this repo. They are shared on Drive: <paste link>.
Results: see results/eegimagenet*.csv
