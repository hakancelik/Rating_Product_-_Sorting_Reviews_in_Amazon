# Rating Product & Sorting Reviews on Amazon

## Project Overview

This project aims to address two critical issues in e-commerce: the accurate calculation of product ratings and the effective sorting of product reviews. By solving these problems, we enhance customer satisfaction, improve product visibility for sellers, and ensure a smooth shopping experience for buyers.

## Problem Statement

In e-commerce, accurately calculating post-sale product ratings is essential for customer satisfaction and for making products stand out. Properly sorting product reviews is also crucial. Misleading reviews can directly affect sales, leading to financial loss and customer attrition. Addressing these issues will help e-commerce sites and sellers increase their sales while providing a seamless purchasing journey for customers.

## Dataset

The dataset contains Amazon product data, including various metadata and product categories. It features user ratings and reviews for the most reviewed products in the Electronics category.

### Variables:
- `reviewerID`: User ID
- `asin`: Product ID
- `reviewerName`: User Name
- `helpful`: Helpful rating score
- `reviewText`: Review text
- `overall`: Product rating
- `summary`: Review summary
- `unixReviewTime`: Review time (Unix timestamp)
- `reviewTime`: Raw review time
- `day_diff`: Number of days since the review
- `helpful_yes`: Number of times the review was marked as helpful
- `total_vote`: Total number of votes for the review

## Tasks

### Task 1: Calculate the Average Rating Based on Recent Reviews and Compare It with the Existing Average Rating

1. **Load the Dataset and Calculate the Product's Average Rating**
   - The dataset includes user ratings and reviews. Calculate the average rating based on these reviews and compare it with the existing average rating.

2. **Calculate the Weighted Average Rating Based on Date**
   - Convert date columns to datetime format and calculate the weighted average rating based on the date of the reviews.

3. **To Observe Which Time Zone It Is In**
   - Determine the time zone of the data to ensure accurate date calculations.

4. **Ratings Given Recently Are Higher**
   - Analyze if recent ratings are higher, which might indicate the product’s popularity.

### Task 2: Determine 20 Reviews to be Displayed on the Product Detail Page

1. **Create the `helpful_no` Variable**
   - The `total_vote` variable represents the total number of up and down votes for a review. Create the `helpful_no` variable to indicate the number of unhelpful votes.

2. **Calculate and Add the `score_pos_neg_diff`, `score_average_rating`, and `wilson_lower_bound` Scores to the Data**
   - Compute the `score_pos_neg_diff`, `score_average_rating`, and `wilson_lower_bound` for each review and add these scores to the dataset.

3. **Identify 20 Reviews and Interpret the Results**
   - Select the top 20 reviews based on the calculated scores and provide an interpretation of the results.

## Installation

To run this project, ensure you have the following dependencies installed:

- Python 3.x
- Pandas
- NumPy
- scikit-learn

You can install the required packages using pip:

```bash
pip install pandas numpy scikit-learn
```
## Usage

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd Rating_Product_-_Sorting_Reviews_in_Amazon
   ```

## Results

The results of the analysis will be saved in the `results` directory. You will find the following:

- `average_rating_comparison.csv`: A CSV file comparing the calculated average ratings with the existing average ratings.
- `review_scores.csv`: A CSV file containing the calculated `score_pos_neg_diff`, `score_average_rating`, and `wilson_lower_bound` for each review.
- `top_reviews.csv`: A CSV file with the top 20 reviews based on the calculated scores.

## Known Issues

- Ensure that the dataset is correctly formatted before running the analysis.
- If you encounter any issues, please check the dataset for missing or malformed data.
- The script assumes that the dataset has been preprocessed correctly; otherwise, errors may occur.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

