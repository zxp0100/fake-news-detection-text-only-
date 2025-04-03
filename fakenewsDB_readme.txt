The fake_news_db.json file contains our entire fake news database, with a total of 68,519 fake news articles. 
The json file includes each single fake news article in our database, saved in a dictionary format, where each entry corresponds to the following: 

* factcheck_url: URL of the original fact-checker article that we scraped. That is, the URL of the article that analyzes and classifies a claim/piece as being true or false.

* claim_reviewed: the text of the claim/piece of information analyzed and classified by the fact checker.

* claim_reviewed_autotranslated_en: the automatic English translation of the claim_reviewed. Some fact checkers' articles are not originally in English. In this column one can find all the original claim_reviewed in English (translated or not).

* factcheck_date_published: To collect this data, we scraped fact checkers’ websites that use the Google claim review system. The factcheck_date_published corresponds to the date of the publication in the Google claim review system.

* website_date_published: the fact-checker article publication date present (or not in case of None) in the fact-checker original website.

* items_reviewed: the URL of the claims/news articles/social media posts being verified by the fact-checker. Sometimes there is more than one claim/article/post being analyzed by the fact-checker, that is why this column contains a list.

* factcheck_classification: original classification given to items_reviewed by the factchecker. Notice that different fact checkers contain different denominations in their classifications for the span between false and true. This column contains this original denomination.

* factcheck_classification_autotranslated_en: not all fact checkers we scraped are in English. Therefore, some classifications had to be automatically translated. This is the column containing all classifications translated to English.

* factcheck_classification_standardized: as mentioned, each fact-checker uses its own classification system. This column standardizes all these different classifications into one of the following categories: ‘false’, ‘unknown’, ‘other’, ‘true’, or ‘satire’. Note that all categories from 'false' and 'misleading' to 'partially false' are categorized as ‘false’, while all categories from 'true' to 'partially true' are included in the category ‘true’. The classification ‘other’ corresponds to claims that we could not attribute to the categories ‘false’ or ‘true’, mostly because they were a perfect mix of true and false affirmations. The category ‘unknown’ corresponds to claims we could not standardize due to a lack of context or problems with automatic translation. The category ‘satire’ corresponds to claims that, despite being mostly false, have a sarcastic purpose. Some claims were not classified/verified by us, and their value is set to None in this column.
