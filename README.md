# Water-Potability-ML-Model
Water Ptability - Safe Drinking Water  
Clean water is one of the world's most precious resources, yet determining if a water source is potable (safe to drink) can be rather difficult. For my project, I wanted to see if Machine Learning could predict water safety based on specific metrics, from pH levels to sulfate concentration.

The Problem:  
The primary goal of this project was to answer the question of "can you reliably predict if water is safe to drink using only its chemical and physical properties?". In the real world, testing every single water source for every possible contaminant is expensive and time consuming. If a machine learning model can accurately flag suspicious water based on standard sensor data then lab testing can be used for more needed cases.

The Investigation: Three Experiments
For this project I ran three different experiments using a Random Forest model algorithm.
I started by filling in missing data gaps with simple averages. This gave a starting accuracy of about 65%.
I realized that water data can have outliers and so by using the median instead of the average and tuning the model’s depth, the accuracy climbed to 67%.

Safety First: In water safety, a False Positive (saying water is safe when it’s actually toxic) is the worst case scenario. I adjusted the model to pay extra attention to the "Safe" samples, ensuring it didn't just take the easy path of predicting everything as "Unsafe."

Key Findings:
After analyzing the data, two main factors showed as the most important factors in determining safety:

Sulfates: This was the #1 predictor. High sulfate levels often correlate with industrial runoff or mineral deposits, which significantly impact potability.

pH Levels: The acidity or alkalinity of the water was the second most vital variable. Even if other minerals are within range, a pH that is too high or too low makes water undrinkable.

Conclusion: While the model reached 67% accuracy, the research shows that water safety is nuanced. These metrics provide a early warning system, but there are larger factors that includes bacteria and local environmental factors that need to be accounted for.

What I Learned:
Through this project, I learned that data cleaning is just as important as the model itself. How you choose to fill in missing information (like a missing pH reading) can change how the model perceives safety. I also learned the importance of Precision vs. Recall in a health related project and that being mostly right isn't good enough, you have to be right about the things that can hurt people.

Why It Matters:
This project demonstrates that data science is largely about decision making. By using models like these, environmental agencies could deploy low cost sensors in remote areas to monitor water in real time. This could be a step towards better water monitoring and ensuring everyone has access to safe drinking water.

Citations:
Dataset is from Kaggle.
Kadiwal, A. (2020). Water Potability [Data set]. Kaggle. https://www.kaggle.com/datasets/adityakadiwal/water-potability
