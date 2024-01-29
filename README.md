# CEO Letter Dimension Identification

## Introduction

This project aims to identify the existence of specific dimensions in letters written by CEOs to shareholders using OpenAI's language model. The model is fine-tuned using provided training datasets and accessed through OpenAI's API. The API key for the tokens to be consumed while fine-tuning needs to be taken from the OpenAI website and the current api_key variable needs to be replaced with your key in the Fine-Tuning section of each model provided in the App folder. The accuracy of the model is evaluated using both in-sample and out-of-sample data.

## Methodology

1. **Load and Preprocess the Data**: Concatenate provided training datasets to create a single training set.
   
2. **Prepare Data for Fine-tuning**: Convert data to a conversational format accepted by OpenAI's API, including system instructions, CEO letter excerpts, and expected dimension identifications.

3. **Fine-tune the Model**: Utilize OpenAI's GPT-3.5-turbo model and fine-tune it with the prepared training data.

4. **Make Predictions**: Use the fine-tuned model to predict dimension identifications for both validation and test datasets.

5. **Evaluate Performance of the Fine-tuned Model**: Compare predicted values with actual values for both in-sample (training) and out-of-sample (validation) datasets.

## Results

### Testing Model Accuracy

The fine-tuned model's accuracy is assessed by comparing its predictions with actual values:

| Attributes   | In-sample Accuracy (Training) | Out-of-sample Accuracy (Validation) |
|--------------|-------------------------------|-------------------------------------|
| Goal         | 0.9                           | 0.833                               |
| Activity     | 0.8                           | 0.75                                |
| Strategy     | 0.8                           | 0.75                                |
| Plan         | 0.9                           | 0.75                                |
| Structure    | 0.9                           | 0.75                                |
| Innovation   | 0.9                           | 0.75                                |
| Tactics      | 0.8                           | 0.333                               |
| Relevance    | 0.3                           | 0.333                               |
| Total (Avg)  | 0.7875                        | 0.6666                              |

### Predicting Dimension Values for Test Set

Using the fine-tuned model, dimension values for the test dataset are predicted:

| Attributes | Accuracy |
|------------|----------|
| Goal       | 0.846    |
| Activity   | 0.692    |
| Strategy   | 0.487    |
| Plan       | 0.513    |
| Structure  | 0.77     |
| Innovation | 0.77     |
| Tactics    | 0.72     |
| Relevance  | 0.28     |
| Total (Avg)| 0.64     |

## Conclusion

The project demonstrates the effectiveness of using OpenAI's language model for identifying dimensions in CEO letters to shareholders, with promising accuracy in both training and validation phases. Further enhancements and fine-tuning could improve performance for future applications.
