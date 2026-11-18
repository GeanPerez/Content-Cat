# ContentCat: Tweet Content Classifier

Team capstone project, Polytechnic University of Puerto Rico (2022).

ContentCat classifies a Twitter user's recent tweets with a fine-tuned multilingual BERT model and shows the results in a Flask web app: enter a handle, get the scored tweets.

## Stack
Python, Flask, TensorFlow/Keras, Hugging Face Transformers (bert-base-multilingual-cased), Tweepy, Docker, Nginx.

## How it works
1. The app fetches recent tweets for a handle through the Twitter API.
2. Each tweet is tokenized (max length 512) and scored by the BERT model.
3. Results render in the web UI.

## Run locally
1. Create `.env.local` with your Twitter developer keys:
   CONSUMER_KEY, CONSUMER_SECRET, ACCESS_TOKEN, ACCES_TOKEN_SECRET
2. `docker compose up --build`

## Note
The trained model weights are too large for GitHub and are not included, so the app needs the weights placed in `CapstoneBertModel/variables/` to run. The Twitter API used in 2022 has since changed, so this repo is kept as a portfolio reference.

## My role
Gean C. Perez Gil: backend and model integration.
