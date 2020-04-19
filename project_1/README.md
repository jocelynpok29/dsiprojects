# dsiprojects
### Overview

This project seeks to identify likely factors influencing participation rates and scores and propose recommendations to increase the participation rates in the chosen state of Alabama.

### Datasets

#### Provided Data

The provided datasets are as follows:

- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2018 ACT Scores](./data/act_2018.csv)
- [2017 Combined Scores](./data/combined_2017.csv)
- [2018 Combined Scores](./data/combined_2018.csv)
- [Final](./data/final.csv)

These data give average SAT and ACT scores by state, as well as participation rates, separately and combined, for the graduating class of 2017 and 2018.

### Data Dictionary

|Feature|Type|Dataset|Description|
|:---|:---:|:---:|:---|
|State|object|sat_2017_df_renamed|The states of the United States of America|
|participation_SAT_2017|int|sat_2017_df_renamed|The participation rates for SAT in 2017|
|evidence-based_reading_and_writing_SAT_2017|int|sat_2017_df_renamed|The mean results from the evidence-based reading and writing component of SAT in 2017|
|math_SAT_2017|int|sat_2017_df_renamed|The mean results from the math component of SAT in 2017|
|total_SAT_2017|int|sat_2017_df_renamed|The total results from the math and the evidence-based reading and writing component of SAT in 2017|
|participation_ACT_2017|int|act_2017_df_renamed|The participation rates for ACT in 2017|
|reading_ACT_2017|float|act_2017_df_renamed|The mean results from the reading subtest of ACT in 2017|
|math_ACT_2017|float|act_2017_df_renamed|The mean results from the math subtest of ACT in 2017|
|science_ACT_2017|float|act_2017_df_renamed|The mean results from the science subtest of ACT in 2017|
|composite_ACT_2017|float|act_2017_df_renamed|The composite score obtained in 2017|
