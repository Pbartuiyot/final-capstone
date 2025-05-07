# Final-Capstone
Kipkorir Pbartuiyot Biegon
Captone Project
Sentiment Analysis of Airbnb Reviews to Inform Dynamic Pricing for Listings in Kenya
Problem Statement
In Kenya, the Airbnb market thrives in cities and surrounding environs like Nairobi, Nakuru and popular coastal destinations like Mombasa and Diani.  However, regions like Kisumu, Lamu, and Maasai Mara face low market penetration. Hosts struggle to attract guests due to a lack of visibility, poor pricing strategies, and insufficiently optimised listings that fail to highlight local attractions. Without data-driven insights, hosts set prices that are either too high, deterring guests, or too low, harming profitability. This limits Airbnb’s growth, stifles local economic development, and misses chances to promote rich heritage and wildlife.
Analysing local demand, proximity to attractions, seasonal events, and guest feedback will help hosts set competitive prices, balancing profitability and occupancy. Additionally, natural language processing can identify gaps in listing quality and provide actionable suggestions for enhancement. This not only maximises hosts' revenue but also strengthens Airbnb’s market reach and promotes Kenya’s diverse tourism to a global audience.
Source for the data 
To address this issue, I will scrape data from Airbnb’s websites and other websites, including booking.com, which offers hosts to list their short-stay rental houses and also allows customers to leave reviews and ratings. Specifically, target listings in key Kenyan regions extracting listing details including nightly prices, review texts, review scores, property types (e.g., apartment, villa), amenities (e.g., Wi-Fi, pool), and location coordinates.
Listing Details: Title, property type (e.g., apartment, house), number of bedrooms/bathrooms, amenities (e.g., Wi-Fi, pool).
Pricing: Nightly rate, discounts, service fees.
Location: County, city, or specific coordinates.
Reviews: Ratings, number of reviews, guest comments.
Host Information: Name, response rate, superhost status.
Availability: Booked/unbooked dates.
Methodology
I will preprocess the raw Airbnb review data by removing noise (e.g., punctuation, emojis etc) and standardizing the text through lowercasing and spell-checking. Using natural language processing (NLP) with tools like NLTK or spaCy, I will tokenize the reviews, remove stopwords, and apply lemmatization to normalize words.
Next, I will extract numerical features from the listings (e.g., price, number of bedrooms) and encode categorical variables (e.g., property type) using one-hot encoding. For sentiment analysis, I will employ BERT to classify reviews as positive, negative, or neutral, assigning sentiment scores ranging from -1 to +1, which will be aggregated per listing to inform pricing analysis. I will then build a regression-based pricing model using ensemble techniques like Random Forest or XGBoost, incorporating sentiment scores along with predictors such as location, demand trends, and competitor prices. To optimize the model, I will tune hyperparameters (e.g., tree depth, learning rate) and validate performance with cross-validation. I will also analyze feature importance to pinpoint key pricing influencers.
To evaluate the model’s effectiveness, I will use metrics like Mean Squared Error (MSE) and R-squared (R²) to ensure accurate price predictions. For interpretability, I will leverage SHAP values to illustrate how sentiment and other features affect pricing decisions. Finally, I will deploy the model as a scalable pricing tool, integrating it with Airbnb host dashboards to enable real-time price adjustments.
