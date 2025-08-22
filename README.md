# Junior ML Engineer Coding Exercise — ML Engineering Focus

Goal: ship a small, production-minded ML package that can be trained and then used to generate predictions in a repeatable way.

What you must build:
1. A reproducible training command that reads config.yaml and writes model artifacts to ./artifacts
2. A prediction command that loads the saved model and writes predictions.csv with columns: id, is_fraud_probability
3. Minimal logging, sensible error handling, and one unit test

Suggested order:
- Implement build_preprocess_pipeline in src/features.py
- Implement train CLI in src/train.py
- Implement predict CLI in src/predict.py
- Add one unit test in tests/test_features.py
- If time remains, attempt a Bonus

Run locally:
- python -m pip install -r requirements.txt
- python -m src.train --config config.yaml
- python -m src.predict --config config.yaml

Data:
- fraud_train.csv (labelled)
- fraud_holdout_unlabelled.csv (unlabelled)

Outputs:
- artifacts/model.joblib and artifacts/metrics.json
- predictions.csv

