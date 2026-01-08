## Milestone 1: Data Preparation ✅

### Objective
Prepare clean and structured datasets for recommendation model development.

### Tasks Completed
- Collected and explored E-commerce dataset
- Removed duplicates and handled missing values
- Cleaned user and product interaction data
- Constructed user–item interaction matrix

### Files
- `data/processed/cleaned_data.csv` – cleaned dataset
- `data/processed/user_item_matrix.csv` – user–item interaction matrix
- `notebooks/data_preparation.ipynb` – data preprocessing notebook

### Status
✔️ Milestone 1 completed successfully

## Milestone 2: Recommendation Model Building

### Objective
Develop and train a recommendation model using the prepared e-commerce dataset.

### Model Selection
A **User–Category Collaborative Filtering** approach was implemented.

- Users are represented by their category-level interactions
- Categories act as items in the user–item matrix(changed the productID to category because of sparsity)
- Cosine similarity is used to compute user similarity

This approach allows similarity computation despite single-product interactions.

### Model Architecture
1. User–Item Matrix (User × Category)
2. Implicit interaction modeling
3. Matrix normalization
4. Cosine similarity for user similarity
5. Top-N recommendation logic
6. Popularity-based fallback for cold-start cases

### Training Process
- Constructed a user–category interaction matrix
- Normalized the matrix using L2 normalization
- Computed user similarity using cosine similarity
- Generated recommendations based on similar users' category preferences

### Evaluation Metrics
- **Matrix Sparsity**
- **Recommendation Coverage**
- **Average User Similarity**

These metrics provide an initial assessment of model behavior given data constraints.

### Key Observations
- Due to single interaction per user, similarity signals are weak
- Recommendations often fall back to globally popular categories
- This behavior is expected for cold-start and sparse datasets

### Limitations
- No repeated user interactions
- No explicit ratings
- Limited personalization

Future improvements include using a richer dataset or switching to a content-based recommendation approach.

### Status
✅ Recommendation model successfully developed and trained  
✅ Initial evaluation completed  
✅ Milestone 2 objectives met


