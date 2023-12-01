<ins><strong>Credit default analysis </strong></ins>
<p> Default rates have always been on the high rise due to harsh economic conditions sometimes. However, there are people who have poor credit scores but still end up getting qualified for more loans. The loan policies sometimes change and these peole get easier leeways to penetrate through the system checks. </p>

<p> Seeing how loan recovery agents and staff of microfinance institutions struggle looking for defaulters made me go into developing a classification model to predict the possibility of loan defaulters. </p>

<p> The goal of this project was to developa classification model which predicts whether a cliemt will default or not going by the lifestyle of the specific client.</p>

<p> One thing to note is that this data is cleaned ad has no any missing alues. However, there are categorical variables with **very high cardinality(number of unique values)**. Using the OneHotEncorder is very counter-intuitive and will result to memory issues. I explored an encoding ,ethod known as Count encoding where the variable is replaced by the value of its count. This help preserves the weigt of classes because label encoding them will result to loss of the class weights. </p>

<p>The modelling process involves a series of pipelines to ensure no data is leaked to the mdoel in the process of featue engineering oor even encoding. Pipelines also automate the whole process of Machine learning beacuse the datav passes through a series of transformers before being finally fit on the final model. The pipelines can only be accessed using scikit-learn which has several integration to mitigate the effects of class imbalance where voting is normally towards the majority side. </p>

<p> The main aim is to reduce the values of False negatives as this will make defaulers become qualified for new loans which is not good. Any tuning to the final model should seek to minimize teh false negative occurrences as much as possible. The final model was the Catboost which is optimized for classification problems and handles the class imbalances pretty well. </p>