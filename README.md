A final project for a Marketing Analytics course, exploring how to generate more diverse recipe recommendations and reduce the concentration of recommendations on popular items.

## Objective

Build and compare recommendation methods for a recipe website, with a particular focus on diversity and novelty. The project examines how the choice of model and recommendation-list length affects the range of recipes suggested to users.

## Data

The analysis uses userвЂ“recipe interaction matrices and recipe ingredient features. The interaction data represents usersвЂ™ preferences, while the ingredient features allow us to measure how different the recommended recipes are from one another.

## Methods

The project compares:

- User-based collaborative filtering with Jaccard similarity.
- Item-based collaborative filtering with cosine similarity.
- A LightFM latent factor model.
- A modified latent factor model with zeroed biases and normalized embeddings.

Recommendations are evaluated at different list lengths using four metrics:

- **Mean Inverse User Frequency:** measures the novelty of recommended recipes based on their popularity.
- **Intra-List Diversity:** measures differences between recipes within a recommendation list using ingredient features.
- **Coverage:** measures the proportion of the recipe catalog recommended across users.
- **Coverage Diversity:** measures how evenly recommendations are distributed across recipes.

## Findings

The latent factor approach improved catalog coverage and coverage diversity compared with the user-based baseline for several recommendation-list lengths. Improvements over the item-based baseline were smaller, while the novelty metric showed little difference.

The results illustrate why recommendation quality should be evaluated along several dimensions: a model may recommend a broader range of recipes without producing a comparable improvement in every diversity or novelty metric.

## Tools

Python, pandas, NumPy, SciPy, scikit-learn, LightFM, RecTools, and Matplotlib.
