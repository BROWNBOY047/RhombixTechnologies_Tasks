📘 Automated Essay Scoring using IELTS Dataset
📝 Overview
This project presents an Automated Essay Scoring (AES) system trained on the IELTS Academic Writing Task 2 dataset. The goal is to evaluate and score essays based on their textual and structural features using machine learning techniques. The system can predict essay scores automatically with reasonable accuracy, making it a helpful tool for learners, instructors, and academic platforms.

📂 Dataset
The dataset used is the IELTS Academic Writing Task 2 Scored Essays Dataset. This dataset contains:

Essays written in response to IELTS prompts.

Scores awarded by human graders, specifically the "Overall" band score (ranging from 0 to 9).

The data is well-suited for supervised learning, with each essay paired with a corresponding numerical score.

🔑 Key Columns
Essay: The original, unprocessed essay text.

Overall: The final score awarded to the essay (target variable).

⚙️ Technologies and Tools Used
Python 3

Pandas for data manipulation

NumPy for numerical operations

scikit-learn for ML modeling, preprocessing, and evaluation

TfidfVectorizer for text feature extraction

RandomForestRegressor as the primary regression model

Google Colab for experimentation and execution

Google Drive for data storage and model persistence

🔁 Workflow Summary
1. Data Loading
The IELTS dataset (a .zip file) was placed in a Google Drive folder and extracted using Colab.

2. Text Cleaning
All essays were lowercased.

Punctuation, special characters, and numbers were removed.

Extra whitespace was stripped to normalize formatting.

Cleaned text was stored in a new column called clean_essay.

3. Feature Engineering
To enhance the model's understanding of each essay's structure, the following features were extracted:

essay_len: Total number of characters.

word_count: Total number of words.

avg_word_len: Average word length.
These features were combined with text features for a hybrid model.

4. Data Splitting
The dataset was split into training and test sets (80% / 20%).

Both textual and numeric features were separated and then recombined for modeling.

5. Model Pipeline Construction
A full pipeline was constructed using scikit-learn:

Text Preprocessing: TfidfVectorizer to convert text to numerical vectors (bigrams, max 5000 features).

Numeric Preprocessing: StandardScaler to normalize the numeric features.

Regressor: RandomForestRegressor trained to predict the overall IELTS score.

The pipeline was designed to handle both numeric and textual data in a unified structure.

6. Model Training
The model was trained on the processed training data using the pipeline.

Training was efficient and took advantage of the Colab GPU where necessary.

7. Model Evaluation
The model's performance was evaluated using:

Mean Absolute Error (MAE): Measures average absolute error in predictions.

Mean Squared Error (MSE): Penalizes larger errors more heavily.

R² Score: Indicates the proportion of variance explained by the model.

Results (on the test set):

MAE: ~0.64

MSE: ~0.70

R² Score: ~0.32

These results are considered reasonable given the small dataset and absence of grammar-specific linguistic features.

8. Model Saving and Deployment
The trained pipeline was saved as a .pkl file for reuse and deployment.

It was uploaded to Google Drive and is ready for download or integration into web applications.

9. Prediction on New Essays
A clean prediction pipeline was implemented to handle single or multiple new essay inputs.

It supports multi-line essays and automatically calculates the required features before making predictions.

🧠 What Makes This Project Special?
Combines textual semantics with quantitative structure features.

Uses a modular, clean pipeline for ease of training and inference.

Designed with real-world use cases like automated grading tools, educational apps, or mock IELTS evaluation platforms in mind.

Built efficiently on Google Colab with cloud storage integration for scalability.

📌 Limitations
The model doesn't yet account for grammar, coherence, or logical structure explicitly.

Trained only on a limited number of essays from the IELTS dataset.

Scoring may not perfectly align with trained human IELTS examiners.

🚀 Future Improvements
Integrate deep learning models (e.g., BERT or RoBERTa) for contextual understanding.

Add grammar and syntax analysis using NLP libraries like spaCy or LanguageTool.

Expand dataset to include more writing tasks and different scoring rubrics.

Deploy as a web API or interactive dashboard using Streamlit or Flask.

💬 Final Words
This project demonstrates a practical application of machine learning in education by automating essay assessment. It's fast, adaptable, and has the potential to evolve into a full-fledged writing evaluation system. Contributions and suggestions are welcome for further enhancement!
