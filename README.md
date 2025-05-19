# SMS Spam Detector

This project builds an SMS spam detection app using a linear Support Vector Classifier (SVC) and TF-IDF vectorization. A Gradio interface is included for interactive text message testing.

## Features

- Classifies SMS messages as either "spam" or "not spam"
- Uses a pipeline with `TfidfVectorizer` and `LinearSVC`
- Handles class imbalance with `class_weight='balanced'`
- Simple web interface built with Gradio for user input and output

## Files

- `gradio_sms_text_classification.ipynb`: Main notebook with Gradio app and model
- `sms_text_classification_solution.ipynb`: Reference notebook
- `SMSSpamCollection.csv`: Dataset containing labeled SMS messages

## Getting Started

1. Clone the repository.
2. Make sure required packages are installed: `scikit-learn`, `pandas`, and `gradio`.
3. Open the main notebook: `gradio_sms_text_classification.ipynb`.
4. Run all cells to train the model and launch the Gradio app.

## Example Test Inputs

- You are a lucky winner of $5000!
- You won 2 free tickets to the Super Bowl.
- You won 2 free tickets to the Super Bowl. Text us to claim your prize.
- Thanks for registering. Text 4343 to receive free updates on medicare.

## Notes

The model was trained on a dataset of 5,572 messages, with a majority labeled as "ham" (not spam). To compensate for class imbalance, `class_weight='balanced'` was added to the LinearSVC model.
