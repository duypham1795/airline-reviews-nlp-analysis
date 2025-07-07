# ✈️ Airline Reviews NLP Analysis

This project performs an in-depth Natural Language Processing (NLP) analysis of over 120,000 airline passenger reviews to uncover insights into customer sentiment, service quality, and operational challenges. It combines modern NLP techniques such as sentiment analysis, topic modeling, and word embeddings with classic exploratory methods.

---

## 📊 Dataset

- **Source**: [Kaggle - 128k Airline Reviews](https://www.kaggle.com/datasets/joelljungstrom/128k-airline-reviews)
- **Content**: Text reviews, numeric ratings, and airline metadata from global travelers.

---

## 🔍 Analysis Overview

### 🧹 1. Data Preprocessing
- Cleaned review text (lowercasing, punctuation removal)
- Tokenization, stopword removal, stemming/lemmatization
- Constructed bigrams
- Converted review ratings to binary sentiment (`positive` vs `negative`)

---

### 📊 2. Exploratory Data Analysis (EDA)

#### 📉 MDS (Multidimensional Scaling)
Visualizes word co-occurrences by semantic themes:

**1. Service & Comfort (Left Side)**  
*Words*: comfort, food, seat, crew, entertainment, service  
*Theme*: In-flight experience, staff friendliness, amenities

**2. Booking, Money & Customer Support (Top-Right)**  
*Words*: book, ticket, refund, money, charge, call, email  
*Theme*: Payment issues, booking process, customer support complaints

**3. Delays, Timing & Logistics (Bottom-Right)**  
*Words*: delay, hour, connect, wait, gate, airport  
*Theme*: Flight punctuality, miscommunication, missed connections

**4. Negative Experiences (Top-Center/Right)**  
*Words*: worst, rude, disappointing, cancel, issue, problem  
*Theme*: Strong expressions of dissatisfaction

---

### 😊 3. Sentiment Analysis
Used both **VADER** and **TextBlob**:

- Clear correlation between review language and star rating
- **Positive reviews** use consistently upbeat language
- **Negative reviews** show unambiguous dissatisfaction

---

### 🧵 4. Topic Modeling (LDA)

Identified 5 coherent topics:

**1. Flight Class & Route Experience**  
→ Comments on business vs economy, especially for routes involving China and Beijing. Mentions of lounges, meals, and seats reflect premium expectations.

**2. International Travel & Seat Quality**  
→ Focused on long-haul flights (Canada, Toronto), comfort, airline quality, and seat experiences.

**3. Delays & Timing Concerns**  
→ Complaints about long delays, customs, and missed connections. Time-related frustrations dominate.

**4. Onboard Cabin Service**  
→ Covers in-flight staff, food quality, and overall cabin environment. Reflects both praise and criticism.

**5. Check-In & Boarding Process**  
→ Issues with check-in, boarding, baggage handling, and interactions with airport staff.

---

### 🧠 5. Word Embeddings (Word2Vec)

Captured three key dimensions:

**1. Personal/Leisure Travel**  
→ Words like *holiday*, *vacation*, *children*, *suitcase*, *journey*  
→ Indicates family trips, travel ease, and enjoyment

**2. Logistics & Timing**  
→ Focused on *layover*, *connection*, *airport*, *Dallas*, *LAX*  
→ Concerns about connecting flights and travel schedules

**3. Negative Sentiment**  
→ *waste*, *stress*, *hassle*, *avoid*, *recline*  
→ Represents dissatisfaction, product complaints, and frustration

---

## 🧠 Key Takeaways

- Positive reviews are clearly positive; negative ones are strongly critical.
- Operational pain points include delays, customer service, and booking/payment problems.
- Service quality (crew, seat, food) is a key driver of satisfaction.
- LDA topics and Word2Vec embeddings reveal hidden dimensions of traveler experience.

---

## 🛠️ How to Run

```bash
# Clone the repository
git clone https://github.com/duypham1795/airline-reviews-nlp-analysis.git
cd airline-reviews-nlp-analysis

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook Airline_Reviews_Comprehensive_Analysis.ipynb
