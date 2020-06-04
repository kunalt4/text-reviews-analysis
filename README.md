# Text Classification of Reviews

Used the **bs4** package to scrape review data from a website from three categories. This textual data was then preprocessed using various text pre-processing techniques including **stopword-removal, normalization and lemmatization.**
Then, we used trained and tested three models on each of the three category datasets, and concluded that Logistic Regression performed the best of those, with accuracies of **79.6%, 88.5% and 87%** on cafe, hotel and restaurant data respectively.

For the next task, we trained the **logistic regression** model on one category, and classified the data of the other two categories.

For this task, our data needs to be preprocessed and the **shape of features** in all three datasets needs to be **identical**. Initally,this was done by combining the datasets and preprocessing then together, and then seperating into different categories. This was later changed into the current method of using the **vectorizer's transform function** to shape the test data according to the train data - which gave slightly better results than the previous method.

Training on **cafe data**, we see similar accuracies of **82%** when the **hotel and restaurant data** is classified.

Training on **hotel data**, we see an accuracy of **85% with cafes**, and **81% with restaurants.**

Training on **restaurant data**, we see an accuracy of **85% with hotels**, and **88% with cafes**.

There is a **slight bias towards positive ratings** in each model. This is expected as we have not accounted for bias in the dataset while classification.

The accuracies of each model lie in a similar range, this might be because all three categories - cafes, restaurants and hotels are pretty similar, so the review text would contain a lot of the same words. This might be different across **different domains**.
