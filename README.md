# fmri-eeg

project/
│
├── data/                   # Original and processed datasets (e.g., ds004504/)
│   ├── raw/                # Original BIDS formatted files or dataset copies
│   └── processed/          # Preprocessed/feature-extracted data (e.g., scalpograms)
│
├── splits/                 # Subject-wise CSV splits for train/test/val
│
├── features/               # Cached feature representations (images or tensors)
│   └── scalpograms/
│
├── src/                    # Core source code
│   ├── data/               # Data loading, preprocessing, augmentation scripts (io_bids.py, dataset.py)
│   ├── features/           # Feature extraction & signal transform utilities (harmonics.py, tf_transform.py, windows.py)
│   ├── models/             # Model architectures (resnet.py, vit.py, gnn.py, etc.)
│   ├── training/           # Training, evaluation, inference scripts (train.py, eval_metrics.py, infer_subject.py)
│   ├── utils/              # Common utility functions, logging, metrics helpers
│   └── analysis/           # Interpretability, robustness, calibration, stats tests scripts
│
├── conf/                   # Experiment YAML configs with Hydra for easy parameter tuning
│
├── runs/                   # Logs, checkpoints, metrics outputs from experiments
│
├── requirements.txt        # Python dependencies (alternative to conda environment)
├── environment.yaml        # Conda environment file for reproducibility
├── README.md               # Project overview and instructions
└── setup.py / pyproject.toml  # Optional - for packaging project as installable module
