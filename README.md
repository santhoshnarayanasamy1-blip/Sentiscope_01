# SentiScope

Real-time sentiment analysis with a Bi-LSTM neural network (TensorFlow/Keras) and word-level explanations, served with Streamlit.

## Run locally (Python 3.11 or 3.12)
```bash
pip install -r requirements.txt
python train.py          # ~5-10 min on CPU, creates artifacts/ (model, vocab, metrics)
streamlit run app.py
```

## Deploy (Streamlit Community Cloud)
1. Run `python train.py` locally, then commit the `artifacts/` folder (about 8 MB).
2. Push the project to a public GitHub repo.
3. share.streamlit.io -> New app -> pick the repo, branch `main`, main file `app.py`.
   Under Advanced settings choose Python 3.11 or 3.12.
4. Paste the resulting URL into the PPT (`--demo`) and the submission.

## Screenshots and PPT
Save four screenshots of the running app into `screenshots/` with these names:
`01_analyze.png`, `02_negative.png` (click "Scathing review"), `03_insights.png`, `04_how_it_works.png`.
```bash
python build_ppt.py --name "Your Name" --reg "Your Reg No" --github "github.com/you/sentiscope" --demo "your-app.streamlit.app"
```

## Structure
`app.py` UI and inference | `train.py` training | `common.py` shared preprocessing | `build_ppt.py` report deck
