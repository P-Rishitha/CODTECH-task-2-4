Name: PODUGU RISHITHA

Company: CODTECH IT SOLUTIONS

ID: CT08DFJ

Domain: Machine Learning

Duration: December 2024 to January 2025

Mentor: NEELA SANTHOSH KUMAR

---

## **Recommendation System Using Matrix Factorization (NMF)**

This repository contains a Python implementation of a **Recommendation System** using **Non-Negative Matrix Factorization (NMF)**. The code demonstrates how NMF can be applied to decompose a user-item matrix into two lower-dimensional matrices, enabling predictions for missing values.

---

### **Overview**

The code performs the following:
1. Initializes a sample user-item matrix, simulating user ratings for items.
2. Applies NMF to decompose the matrix into two factors: **user features** and **item features**.
3. Reconstructs the original matrix to predict missing values, which can be used for recommendations.

---

**Output**

![Screenshot 2025-01-05 13 08 40](https://github.com/user-attachments/assets/f356f155-c3b7-4786-922c-14ab651601c7)

---

### **Steps in the Code**

1. **User-Item Matrix**  
   A small user-item matrix `R` is created with some missing ratings (represented as zeros). Each row corresponds to a user, and each column corresponds to an item.

2. **Applying NMF**  
   - **Non-Negative Matrix Factorization (NMF)** is applied using `sklearn.decomposition.NMF`.
   - The matrix `R` is decomposed into two non-negative matrices:
     - `W`: User feature matrix.
     - `H`: Item feature matrix.

3. **Reconstructing the Matrix**  
   - The original matrix `R` is approximated by multiplying `W` and `H`.
   - Missing values (zeros) in the original matrix are predicted in the reconstructed matrix `R_predicted`.

4. **Predicted Ratings**  
   The reconstructed matrix `R_predicted` contains both original ratings and predicted values for missing entries, which can be used to make recommendations.

---

### **Requirements**

- Python 3.7 or higher
- NumPy
- scikit-learn

Install dependencies using:
```bash
pip install numpy scikit-learn
```

---

### **Usage**

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/nmf-recommendation-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd nmf-recommendation-system
   ```
3. Run the script:
   ```bash
   python nmf_recommendation.py
   ```

---

### **Applications**

- **Movie Recommendations:** Predict user ratings for movies they haven’t rated.
- **Product Recommendations:** Suggest products based on user preferences.
- **Personalized Services:** Recommend content or services tailored to user interests.

---

### **Extensions**

- Replace the sample matrix with a real-world dataset, such as movie ratings or e-commerce data.
- Experiment with different numbers of components (`n_components`) for improved accuracy.
- Visualize recommendations using heatmaps or charts.
- Add evaluation metrics like RMSE or MAE to measure prediction quality.

---

### **Contributing**

Contributions are welcome! Feel free to:
- Extend the code to handle larger datasets.
- Add support for sparse matrices to save memory.
- Implement additional matrix factorization techniques.
