# mobilerec
This repository contains the baselines for mobilerec dataset.
# Requirements

- Python 3.8 or above
- RecBole 1.1.1
- Pytorch



# Data Fields
|   **Feature**  |                                                                           **Description**                                                                          |
|:--------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|       uid      | 16-characters alphanumeric uid represents a user uniquely. It also anonymizes the user.<br>Example: Aj0Sm6myfh6YN3Rn, 3pZUhksFIcLjEXtl, dvx0dqXTKtHUmY3O           |
|   app_package  | Represents android package name of an application and uniquely identifies an application.<br>Example: com.google.android.calculator, com.king.crash, org.wikipedia |
|    app_name    | Title of the app as displayed on Google Play. <br>Example: Candy Crush Saga, MONOPOLY - Classic Board Game                                                         |
|     review     | Text review given by a user to an application                                                                                                                      |
|     rating     | Numeric rating the user has given to an application.<br>Example: 5, 2, 1, 4                                                                                        |
|      votes     | The number of users who found this review helpful.\\ Example: 1, ..., 6, ...                                                                                       |
|      date      | The date of the specific user/item interaction, i.e., review date. <br>Example: October 21, 2018, November 4, 2021, January 16, 2021                               |
|  formated_data | The date of the specific user/item interaction. (review date in YYYY-MM-DD format). <br>Example: 2018-10-21, 2021-11-04, 2021-01-16                                |
| unix_timestamp | The review date converted into unix timestamp. <br>Example:1.540094e+09<br>	1.547788e+09, 1.610773e+09                                                              |
|  app_category  | The category of the application.<br>Example: Action, Puzzle, Simulation, Role Playing                                                                              |

# Results
| Method Metric | Hit@1  | Hit@5  | Hit@10 | Hit@15 | Hit@20 | NDCG@5 | NDCG@10 | NDCG@15 | NDCG@20 |
|---------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|
|      Pop      | 0.0027 | 0.0086 | 0.0151 | 0.0208 | 0.0256 | 0.0056 |  0.0077 |  0.0092 |  0.0103 |
|     SASRec    | 0.0026 | 0.0098 | 0.0181 | 0.0242 | 0.0295 | 0.0061 |  0.0088 |  0.0104 |  0.0117 |
|    ElecRec    | 0.0020 | 0.0094 | 0.0174 | 0.0237 | 0.0293 | 0.0056 |  0.0082 |  0.0098 |  0.0112 |
|    Bert4Rec   | 0.0024 | 0.0083 |  0.014 | 0.0183 | 0.0221 | 0.0054 |  0.0072 |  0.0083 |  0.0092 |
|      HGN      | 0.0012 | 0.0054 | 0.0096 | 0.0132 | 0.0165 | 0.0033 |  0.0046 |  0.0056 |  0.0064 |
|      SINE     | 0.0022 | 0.0087 | 0.0163 | 0.0228 |  0.028 | 0.0054 |  0.0078 |  0.0095 |  0.0107 |
|   LightSANs   | 0.0024 | 0.0102 | 0.0172 | 0.0227 |  0.028 | 0.0062 |  0.0085 |  0.0099 |  0.0112 |
|    GRU4Rec    | 0.0021 | 0.0086 | 0.0153 |  0.021 | 0.0261 | 0.0053 |  0.0074 |  0.0089 |  0.0102 |
|     GCSAN     | 0.0024 | 0.0094 | 0.0161 | 0.0214 | 0.0266 | 0.0059 |  0.0081 |  0.0095 |  0.0107 |
