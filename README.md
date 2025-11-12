
🍽️ Zomato Restaurant Recommendation System

This project builds a **content-based restaurant recommendation system** using the **Zomato Bangalore Restaurants dataset** from Kaggle.
It recommends restaurants that are **most similar in reviews, cuisine, and user ratings** to a given restaurant name — using **Natural Language Processing (NLP)** and **machine learning techniques**.



 🚀 Project Overview

The recommendation system analyzes restaurant reviews, cleans the text, and applies **TF-IDF vectorization** to capture key terms and phrases from user feedback.
Using **cosine similarity**, it finds restaurants with similar review patterns and sorts them based on normalized mean ratings.



🧠 Tech Stack
Programming Language:Python
Libraries Used:

`pandas`, `numpy` — Data cleaning and manipulation
`matplotlib`, `seaborn` — Visualization
`nltk` — Text preprocessing (stopwords removal, tokenization)
`scikit-learn` — TF-IDF vectorization, MinMaxScaler, cosine similarity
`re`, `string` — Regex and punctuation removal



 📊 Dataset

Dataset Name: [Zomato Bangalore Restaurants](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants)

File: `zomato.csv`

 Key Features:

* Restaurant Name (`name`)
* Online Order Availability (`online_order`)
* Table Booking Availability (`book_table`)
* Rating (`rate`)
* Cuisines (`cuisines`)
* Cost for Two (`approx_cost(for two people)`)
* Reviews List (`reviews_list`)
* Restaurant Type and City


🧹 Data Preprocessing

1. Removed duplicates and missing values
2. Cleaned cost and rating fields
3. Normalized mean ratings to a **1–5 scale**
4. Converted Yes/No fields to Boolean
5. Preprocessed reviews:

   * Lowercased text
   * Removed punctuation
   * Removed stopwords
   * Removed URLs
6. Dropped unnecessary columns like `address`, `menu_item`, etc.

 🧮 Model Workflow

1. TF-IDF Vectorization of cleaned reviews (`unigrams` and `bigrams`)
2. Cosine Similarity computation across all restaurants
3. For a given restaurant:

   * Retrieve top-30 similar restaurants based on review similarity
   * Sort by normalized mean rating
   * Return top-10 restaurant recommendations



 💡 Example Output


TOP 10 RESTAURANTS LIKE "Pai Vihar" BASED ON REVIEWS:

          name                 cuisines        Mean Rating    cost
0   Taaza Thindi              South Indian        4.73        300.0
1   Halli Mane                South Indian        4.62        400.0
2   MTR 1924                  South Indian        4.47        500.0
3   Brahmins' Coffee Bar      South Indian        4.55        200.0
4   Vidyarthi Bhavan          South Indian        4.45        450.0



🧩 How to Run

1️⃣ Clone the Repository

bash
git clone https://github.com/your-username/zomato-restaurant-recommendation.git
cd zomato-restaurant-recommendation


2️⃣ Install Required Libraries

bash
pip install -r requirements.txt


 3️⃣ Download the Dataset

Download from [Kaggle Zomato Dataset](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants)
and place `zomato.csv` in the project root directory.

 4️⃣ Run the Script

bash
python main.py




🧾 Example Function Call

python
recommend('Pai Vihar')


Output:

Displays top 10 restaurants similar to “Pai Vihar” based on reviews and ratings.



📈 Future Improvements

* Add hybrid filtering (combine content + collaborative methods)
* Include sentiment analysis of reviews
* Build an interactive Streamlit dashboard
* Deploy model as a web app (Flask / FastAPI)


