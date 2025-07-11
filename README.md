# TrizahNzioka-association-mini

## Objective
This project applies Association Rule Mining using the Apriori algorithm to uncover patterns in fake movie-watching data. The goal is to simulate transactional data and generate meaningful "if-then" rules based on viewer habits.

## Dataset
I created 10 fake transactions. Each transaction contains 2–5 action movies watched by a user.  
The pool of movies includes:

- John Wick  
- Die Hard  
- Avengers  
- The Dark Knight  
- Inception  
- Mission Impossible  
- Gladiator  
- Mad Max  
 

Each transaction represents one user's movie-watching session.

## Method and Tools
1. **Data Encoding**  
   Transactions were converted into one-hot encoded format using pandas, turning each movie into a column (1 = watched, 0 = not watched).

2. **Frequent Itemsets (Apriori)**  
   I used the Apriori algorithm from `mlxtend` to identify frequent combinations of movies using:
   - Minimum support: 0.3 (appears in at least 3 of 10 transactions)

3. **Association Rules**  
   I then generated association rules using:
   - Metric: confidence  
   - Minimum confidence threshold: 0.7

## Sample Rules and Explanations

**Rule 1:**  
If someone watches John Wick and Mission Impossible, there is a 75% chance they will also watch Die Hard.

**Explanation:**  
People who enjoy fast-paced spy/action films often also enjoy action classics like Die Hard. A recommendation system could use this to suggest Die Hard to similar viewers.

**Rule 2:**  
If a user watches Inception and The Dark Knight, they are likely to also watch Avengers.

**Explanation:**  
Viewers who enjoy mind-bending and intense action films tend to also watch big-budget superhero blockbusters like Avengers. This rule supports cross-genre recommendations.

## Tools Used
- Python  
- pandas  
- mlxtend  
- VS Code or Jupyter Notebook  

## Files Included
- `association_mining.ipynb`: Full Python code  
- `README.md`: Project explanation and rule interpretations

## Conclusion
This mini-assignment demonstrates how Apriori-based association rule mining can find hidden patterns in viewing behavior. Such techniques are useful for building recommender systems in platforms like Netflix, Amazon, or YouTube.
