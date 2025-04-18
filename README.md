**ROC** stands for Receiver Operating Characteristic curve. It plots TPR vs FPR.

TPR (True Positive Rate) = how many actual positives you correctly identified (Also called Recall)

FPR (False Positive Rate) = how many actual negatives you incorrectly predicted as positive.

**Example**

Suppose you get 5 emails : the model predicted probabilities for each email.

If you set a threshold  of 0.5:

3 emails are predicted as spam, 2 emails are not.

But instead of picking just one threshold, ROC explores all thresholds (from 1.0 to 0.0) and shows how TPR and FPR change

================================================================================

The term “Receiver Operating Characteristic” comes from World War II!

Back then, engineers were working on radar systems. Their goal was to help a radar operator (aka the “receiver”) distinguish enemy aircraft (signal) from background noise (non-signal).

They created a curve to visualize this:

True Positive Rate (TPR) → how often the radar correctly detects real planes

False Positive Rate (FPR) → how often the radar mistakenly "sees" something that isn’t a plane

This trade-off was plotted as a curve… and thus, the Receiver Operating Characteristic curve was born

===============================================

**Choosing the right threshold** 

It depends on your real-world goals—what’s worse: a false positive or a false negative?

**Spam Classification** → You want high precision, Increase the threshold 

False Positive (FP) = A legit email marked as spam (bad user experience)

False Negative (FN) = A spam email not caught (annoying, but user can delete it) which is ok compared to FP

**Healthcare** (e.g., cancer detection) → You want high recall, Lower the threshold

False Negative (FN) = Missed a real disease → serious or even fatal

False Positive (FP) = Patient flagged for more tests unnecessarily

**Conclusion:**

Improving precision often lowers recall, and vice versa. So it all depends on what's more costly: a false alarm or a missed case.
