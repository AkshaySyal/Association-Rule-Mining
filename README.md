# Association-Rule-Mining
This project involved developing a Python program to convert kosarak.dat itemset data into a sparse ARFF format, subsequently loading the generated file into Weka for association rule mining using the FP-Growth algorithm, and analyzing the performance of these conversion and mining steps.

# Problem Statement
![image](https://github.com/user-attachments/assets/53234500-64e2-42d9-888b-1fdbcc0e9686)


# Solution Summary
- Focused on preprocessing and analysis of the **kosarak.dat** large itemset dataset for **association rule mining**.

- **Data Preprocessing**:
  - Developed Python program to convert raw `kosarak.dat` to **sparse ARFF format**.
  - Processed:
    - 990,002 transactions
    - 41,270 unique attributes
  - Key insight:
    - Raw data contained **duplicate item IDs within transactions**.
    - Addressed by converting item lists to sets for uniqueness.
  - Conversion time: **~43 seconds**.

- **Loading and Mining**:
  - Loaded sparse ARFF file into **Weka** in **~12 seconds**.
  - Used Weka’s **FP-Growth** implementation.
  - Parameters:
    - Minimum support count: 49,500
    - Minimum confidence: 99%
  - Discovered **2 association rules**.

- **Performance Insights**:
  - FP-Growth execution time: **~2 seconds per run** after initial runs.
  - Major time cost was in **data preparation and loading (~55 seconds total)**, not algorithm execution.

- **Conclusion**:
  - Efficient data cleaning and preparation are critical for large-scale association rule mining.
  - Mining phase itself is fast when using optimized tools like FP-Growth in Weka.
