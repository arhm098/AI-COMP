
Preprocessing:
The dataset initially presented a challenge with mixed categorical and textual information. Given the time constraints, we decided to focus exclusively on categorical data, mapping ordinal values based on their weights. Multiple algorithms, including attempts at ensemble learning, were employed, but unfortunately, no meaningful results were obtained. Uncertainty initially surrounded the choice of the target variable, wavering between "Resolution_Status" and "Product." Ultimately, we settled on "Product" due to the lack of clarity in the description. Textual data underwent analysis using various Sentence to Vec models, and a neural network classifier was applied to assess its implications. Despite the option for one-hot encoding (OHE) the textual data, it was deemed impractical within the given time frame. Rows with seemingly irrelevant features, such as 'Resolution_Status,' 'Industry_Risk,' 'Resolution_Type,' and others, were dropped as they were either demographic or ID-related, contributing minimally to the classification task.

Model and Results:
For the final model, a neural network was chosen, and the word embedding model from https://huggingface.co/hkunlp/instructor-base was utilized. This model proved to be effective in capturing the semantic information from the textual data. The exclusion of certain features, including 'ZIP_code,' 'State,' 'Company,' 'Date_received,' 'Date_sent_to_company,' 'Complaint_ID,' 'Submitted_via,' and others, contributed to a streamlined and more focused classification process. The decision to prioritize the 'Product' variable as the target enhanced the model's interpretability.

Due to the time it took for the neural network and the imposed constraints, we were unable to obtain results for the model but the pipelines are set up.# AI-COMP

we found the issues in test data, and there was not enough time to fix that.

Also we concated a little frotend but again not enough time to put together everything.
