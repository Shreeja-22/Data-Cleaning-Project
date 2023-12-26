# Web Scraping and Data Cleaning of NewEgg Product Reviews

### Introduction
NewEgg stands out as a widely used online store, especially for electronic products, offering a broad range of choices at competitive prices. The website caters to both tech enthusiasts and everyday consumers seeking trustworthy electronic goods. In this project, our focus was on gathering and organizing product reviews from NewEgg, aiming to create a well-structured dataset for analysis.

By systematically extracting and cleaning these reviews, we aimed to uncover valuable insights into customer opinions and satisfaction levels regarding electronic items. This initiative not only helps users make informed purchasing decisions but also contributes to a deeper understanding of the overall product landscape on NewEgg. Through the streamlined dataset, we aim to empower users with accessible and clear information, facilitating a more confident and informed online shopping experience on the NewEgg platform.

### Dataset Description
The dataset, consisting of 5500 rows and 19 columns, holds crucial information
about various products, their ratings, reviews, and additional details.
The dataset includes the following variables:
1. product: Name of the product
2. ratingCount: Total number of ratings or reviews
3. aveRating: Average rating based on user reviews
4. numRating1-numRating5: Ratings ranging from 1 to 5 eggs
5. currentPrice: Current price of the product
6. revname: Name of the reviewer
7. ownership: Duration the seller owned the product
8. rev_verified: Binary variable indicating if the review is verified
9. revdate: Date of the review
10. revstars: Rating given by the reviewer in stars
11. revtext: Text of the review
12. revhelp: Number of users who found the review helpful
13. qa: Number of questions and answers related to the product
14. manufresponse: Binary variable indicating if the manufacturer responded
15. id: Identifier for the product 

### Steps taken to clean the data
Every column in this dataset has been cleaned individually to ensure that all the variables we deal with for our convenience are numeric (except product). The cleaning was performed using Python libraries - NumPy and Pandas. NumPy is a powerful Python library for numerical computing, providing support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions to operate on these arrays. Pandas, on the other hand, is a versatile data manipulation and analysis library that simplifies working with structured data, offering data structures like DataFrame for efficient data handling and analysis in Python.

Following are the documented steps that we took to clean our dataset:
1. Dropped Variables:
- numRating1-numRating5 were dropped as they were deemed unnecessary for the analysis.
2. Renamed Variables:
- Leading spaces in variable names were eliminated to enhance readability.
3. Cleaned currentPrice:
- Removed '$' and ',' from the string.
- Converted the variable to float type.
4. Cleaned ratingCount:
- Followed the same approach as with currentPrice to ensure consistency
and accuracy.
5. Cleaned revstars:
- Removed the non-numerical part "rating rating-" from the variable.
- Converted the variable to an integer type, handling missing values with NaN.
6. Processed revhelp:
- Split the variable into 'help' and 'help_total'.
- Removed non-numeric characters from 'help' and converted it to float.
- Filled missing values with zeros.
7. Cleaned qa:
- Followed the same approach as with revhelp to clean qa.
- Created and cleaned two new variables, 'quest' and 'answ'.
8. Assessment:
- Ran df.describe() and df.info() to assess the data after cleaning.

### Conclusion
To summarize our project, the thorough cleaning process has made the dataset suitable for in-depth exploration and analysis, providing valuable insights into the details of product reviews on NewEgg. The visualizations, along with statistical descriptions, have allowed for a detailed examination of individual product features and a comprehensive assessment of customer satisfaction trends.
The achievement of our current goals highlights the dataset's effectiveness in revealing patterns and guiding decision-making. However, considering the ever-changing nature of online commerce, it is crucial to stay updated on evolving consumer preferences and market trends. Consequently, future analyses and potential data collection efforts may be necessary to address new questions and objectives.
Moreover, the flexibility of our approach ensures that the dataset remains a reliable tool for understanding the dynamic relationship between consumer opinions and product performance on NewEgg. Continuously refining and expanding our analytical methods will help maintain the dataset's relevance in the constantly shifting landscape of online retail. This ongoing process positions the project not just as a snapshot of the present but as a foundation for continual and evolving investigations into the complex dynamics of electronic product reviews on NewEgg.
