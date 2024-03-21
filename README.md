# Song-Recommendation

This project utilizes Streamlit and Python to recommend similar songs based on user input, including artist, album name, genre, or song name. The dataset consists of 11400 rows of music data

install libraries:
pip install pandas numpy seaborn matplotlib streamlit


Additionally, you'll need to install tfidVector and NearestNeighbors. Ensure they are installed correctly; if they are custom libraries, provide instructions for installation.

Run the following command to execute the application: 
streamlit run app.py

Determine Filter Column:

The function first determines the column to filter based on the user input. It considers columns such as "artists," "track_name," "album_name," and "track_genre."
TF-IDF Vectorization:


It then utilizes TF-IDF vectorization to convert the textual features of the songs into numerical vectors. This process is crucial for finding similarity between songs based on their textual attributes.
Nearest Neighbors Model Fitting:

Next, it fits a Nearest Neighbors model using the TF-IDF matrix generated from the textual features. This model will help identify the most similar songs to the input.
Filtering Data:

The function filters the dataset based on the user input value for the determined column. If matching entries are found, it proceeds to recommend similar songs.
Finding Similar Songs:

For each matching entry, the function utilizes the Nearest Neighbors model to find the most similar songs. It excludes the input song itself from the recommendations.
Displaying Recommendations:

Finally, it prints the recommended track names, ensuring uniqueness to avoid duplicates. It returns the recommendations for further processing or display.
This function can be integrated into a Streamlit application or used as part of a command-line interface to provide song recommendations based on user input.

