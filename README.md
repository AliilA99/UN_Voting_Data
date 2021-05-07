# United Nations Voting Data
This repository is part of a machine learning research project conducted by Ali Cherchar, undergraduate student at the University of Virginia (UVA), and Tianxi Li, assistant professor in the department of statistics at UVA. This research project was made possible thanks to the Undergraduate Student Opportunities in Academic Research, also known as the USOAR program at UVA.

# Dataset
The original dataset is available [here](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/LEJUQZ) and contains roll-call votes in the United Nations General Assembly from 1946 to 2019 (sessions 1 - 75).

# Files 
* `relationships_dot.rds` : R list containing 24 (202 * 202) adjacency matrices. Each matrix contains voting relationships between countries (a number between -1 and 1) which was obtained by applying the dot (.) product of vectors

* `relationships_IsingFit.rds` : R list containing 23 (201 * 201) adjacency matrices. Each matrix contains voting relationships between countries (a number equal to 0 or 1) which was obtained by applying the IsingFit model

Notes:
  1. The original dataset contains voting information from 1946 to 2019 with the exception of 1964. The year 2019 was discarded during the data cleaning phase. Therefore, the dataset used for the study contains 72 different matrices (for 74 years) which were grouped by 3 leaving us with 24 adjacency matrices in total.
  2. IsingFit does not allow countries that don't have a voting similarity with at least one other country during the entire period of time. This is why the dimension of adjacency matrices is (201 * 201) instead of (202 * 202).
  3. 2016, 2017, and 2018 were discarded when using IsingFit leaving us with 23 adjacency matrices in total.

# Contact
If you have any questions on this project, feel free to email me at ac5qm@virginia.edu.
