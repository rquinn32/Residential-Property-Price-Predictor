# COMP47350-Data-Analytics-Project
Data Analytics Project for COMP47350

## Project Details

This project focuses on data understanding, preparation, model training and evaluation for a particular problem and dataset.

The data comes from the Residential Property Price Register (RPPR) (https://www.propertypriceregister.ie/website/npsra/pprweb.nsf/page/ppr-home-en). The Residential Property Price Register is produced by the Property Services Regulatory Authority (PSRA). It includes Date of Sale, Price and Address of all residential properties purchased in Ireland since the 1st January 2010, as declared to the Revenue Commissioners for stamp duty purposes. 

In this analysis, **we focus on using the data collected by RPPR to build a data analytics solution for residential property price prediction**. The target feature for this task is the Price. 

Each group will work with a different subset of the data.  There is a train csv file and a test csv file for each group. The CSV file is named using the format: **ppr-[your-group-contact-ID].csv**, e.g., **ppr-group-12345-train.csv** and  **ppr-group-12345-test.csv** are the 2 data files for a group with id 12345. You need to work with the CSV files corresponding to your group, available from this [[link]](https://drive.google.com/drive/u/2/folders/1xhvlob23xQvnH-mC5JfaXpjqihZqKNHy). There are 5 parts for this project. Each part has an indicative percentage weight of contribution to the final grade, given in brackets, e.g., part (1) has a weight of 25% shown as [25/100]. 


**(1). [25/100] Prepare a Data Quality Report for your training CSV file.**
Use only the training set CSV for data understanding and cleaning. Keep the test set CSV aside for now.

 Below you have a set of guideline steps. All the steps need to be implemented with Python code.

    - Initial data checks, e.g., how many rows and columns your dataset has, print a few rows.
    - Convert the features to their appropriate data types (e.g., decide which features are more appropriate as 
    continuous and which ones as categorical types). You may revisit this decision once you understand the data better, but you will need to take a final decision on the data type of each feature in your Data Quality Plan in part (2).
    - Look for duplicate rows and columns. Consider whether it makes sense to keep them or drop them.
    - Look for constant columns. Consider whether it makes sense to keep them or drop them.
    - Save your updated/cleaned data frame to a new CSV file with a descriptive name (e.g., ppr-group-12345-train-cleaned.csv).
  
    For the updated CSV and data frame (after column/row removal):
    - Prepare tables with descriptive statistics for all the features.
    - Prepare plots for all the features.
    - Discuss your initial findings from the tables and plots.
    - Summarise your findings into a single Data Quality Report (DQR) PDF file. 
    
    The notebook provides all the detailed steps and analysis with code, while the DQR PDF report is a summary of findings and contains no Python code, but tables/plots/images are allowed.
    The PDF report should focus on the key issues identified in the data and discuss potential strategies to handle them (max 5 pages of text + unlimited appendix for tables and plots). The report should be concise and complete, the goal is not to make it long for the sake of length, but to cover all the important aspects of the features. To keep the report concise, you can have all tables and plots in an appendix, and the main body of the report is the summary of key findings from analysing the dataset.

(2). **[15/100] Prepare a Data Quality Plan for the cleaned CSV file.**

    - Mark down all the features where there are potential problems or data quality issues.
    - Propose solutions to deal with the problems identified. Explain why did you choose one solution over 
     others. It is very important to provide justification for your thinking in this part and to list potential solutions, including the solution that will be implemented to clean the data.
    - Apply your solutions to obtain a new CSV file where the identified data quality issues were addressed. You need to take a final decision on feature types (eg for each feature, decide data type - whether you will use it as a continuous or categorical feature). There should be no more NaN feature values after this step. The DQP needs to list every single feature, its data type and the issues identified, plus solutions applied to clean the feature.
    - Save the new CSV file with a self-explanatory name (e.g., ppr-group-12345-train-clean-final.csv). 
    - Save the Data Quality Plan (DQP) to a single PDF file (max 5 pages + unlimited appendix).
        
(3). **[15/100] Exploring relationships between feature pairs.**

    - Choose a subset of features you find promising and plot pairwise feature interactions (e.g., 
    continuous-continuous feature plot or continuous-categorical plots or correlation plots). 
    Explain your choices.
    - Discuss your findings from the plots above. Do you find any features or feature combinations that are predictive of the target outcome? 
    - Explain in plain words (a short text paragraph) the story of your findings so far.
    
(4). **[15/100] Creating new features.**

    - Transform or combine the existing features or add new features from external data sources (e.g., CSO), to create a few new features (at least 3 engineered features) with the aim to better capture the problem domain and to  predict the target outcome. Be careful of potential data leakage and of features that do not generalise to new data (where we do not have the target label, but we try to predict it).
    - Justify the steps and choices you are making. In the grading, consideration will be given to the creativity and domain knowledge shown in preparing the new features. Use code to show that your new features are indeed useful for the target prediction problem. 
    - Add these features to your clean dataset and save it as a CSV file with a self-explanatory name (e.g., ppr-group-12345-train-engineered.csv). 

(5). **[30/100] Training and evaluating prediction models.**

    - Apply the same data cleaning steps and new feature creation to your test set. Save your new test CSV file.
    - On the cleaned training set, train a predictive model to predict the target feature (Price), using the descriptive features selected in the previous section (4). You may use any model covered in the course (e.g., Linear Regression, Decision Trees, Random Forests, etc.).
    - Can you interpret the model? Discuss any knowledge you can gain in regard of the working of this model.   
    - Compute at least 3 relevant evaluation measures on the training set. Compare these results with the evaluation results obtained when using the hold-out test dataset for predictions, and when using cross-validation. Discuss your findings and identify any signs of overfitting or underfitting.
    - Propose new ideas to improve your predictive model (e.g., by using further data prep such as: feature selection, feature re-scaling, creating new features, combining models, using other domain knowledge, reformulating the prediction task, etc). Show how your ideas actually work in practice (with code), by training and evaluating your proposed models. Summarise your findings so far. 
