# Sleep-Stages-Classifier
Deep learning classifier (CNN + Bi-LSTM) for 4-stage sleep classification using only ECG from the MESA sleep study dataset.

# Overview
The primary challenge addressed in this version is the severe class imbalance (low prevalence of Deep and REM stages), resolved through strategic oversampling and Focal Loss optimization.

**Pipeline:**
1. Dataset Access & Loading: MESA Sleep Study (ECG @ 256Hz)
2. Signal Preprocessing: Notch filtering and Z-score normalization
3. Multi-Scale Feature Extraction: Extraction of raw waveforms and Context-Aware HRV features (5.5-minute windows)
4. Data Balancing: Implementation of WeightedRandomSampler to address severe class imbalance
5. Hybrid Architecture: Deep 1D-CNN for morphology + Bidirectional LSTM for temporal dependencies
6. Advanced Optimization: Focal Loss and Cosine Annealing Learning Rate scheduling
7. Performance Evaluation: Precision-Recall analysis and Confusion Matrix validation

**Dataset**
Multi-Ethnic Study of Atherosclerosis (MESA)

**How to Run**
- Install dependencies: *pip install torch mne neurokit2 scikit-learn*
- Update the *DATA_DIR* in the notebook to point to your local .edf and .xml files.
- Run *sleep_stage_classification.ipynb*.
