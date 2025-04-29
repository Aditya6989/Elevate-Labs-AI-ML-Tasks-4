1. How does logistic regression differ from linear regression?
While both use similar math under the hood, their goals are different.
Linear regression predicts a number (like house price).
Logistic regression predicts a probability that something falls into a class (like spam vs. not spam).

2. What is the sigmoid function?
The sigmoid function takes any number (positive or negative) and squashes it into a range between 0 and 1.
This is super useful because it lets us interpret the output as a probability. For example, a score of 0.8 means there's an 80% chance the input belongs to class 1.

3. What is precision vs recall?
These are two ways to look at how good your predictions are:
Precision: Of all the times we predicted "yes", how many were actually "yes"? (Less false alarms)
Recall: Of all the actual "yes" cases, how many did we catch? (Fewer missed cases)

4. What is the ROC-AUC curve?
The ROC curve shows how good your model is at telling apart the classes.
It plots:
True positive rate (recall) vs.
False positive rate at various thresholds.
The AUC (Area Under Curve) gives you a single number between 0 and 1.
Closer to 1 = better model
0.5 = random guessing

5. What is the confusion matrix?
It’s a simple table that shows:
What you predicted vs. what was actually true.
There are 4 cells:
True Positive: You said "yes", and it was "yes".
False Positive: You said "yes", but it was "no".
True Negative: You said "no", and it was "no".
False Negative: You said "no", but it was "yes".

6. What happens if classes are imbalanced?
If one class is way more common than the other (like 95% vs. 5%), your model might just predict the majority class and still look “accurate”—but it's actually doing a bad job.
This can hide poor performance on the minority class (like fraud detection, disease diagnosis). That’s why metrics like precision, recall, and AUC are better than just accuracy here.

7. How do you choose the threshold?
By default, logistic regression uses 0.5—if the probability is above that, it predicts class 1.
But in real life, you might want to change it:
Lower threshold if you want to catch more positives (higher recall)
Raise threshold if you want to avoid false alarms (higher precision)

8. Can logistic regression be used for multi-class problems?
Yes! It can handle more than two classes using strategies like:
One-vs-Rest (OvR): Train one model per class.
Multinomial: A more math-heavy version that handles all classes together.
Libraries like scikit-learn handle this for you automatically.