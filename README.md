# AIUT

This article provides executables of all frameworks and all datasets used in our research of Approximate High Utility Pattern Mining.

The executables include all the frameworks, such as AIUT, AHUPM, AHUPM\*, IUOIL−, HUOMIL−, PULM, DUOCA\*−, and PIDUL\*, and all the datasets which are used in our experiment: Accidents, Chess, Mushroom, Kosarak, AEP, AQ, OnlineRetail, PAMAP, PowerC, T10I4DxK, and TxI4D1000K.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the name of the executable for each algorithm is as follows:

| Original Name   | AIUT | AHUPM | AHUPM*     | IUOIL−  | HUOMIL−  | PULM | DUOCA*−  | PIDUL* |
| --------------- | ---- | ----- | ---------- | ------- | -------- | ---- | -------- | ------ |
| Executable Name | AIUT | AHUPM | AHUPM-STAR | IUOIL-  | HUOMIL-  | PULM | DUOCA-   | PIDUL  |

Note that AHUPM* is a variant of AHUPM that applies the pattern-specific tolerance factor of AIUT instead of the fixed tolerance factor. Since the symbol "*" cannot be used in file names, its executable is named AHUPM-STAR.

2. The parameters of the executables are as follows:

For AIUT, AHUPM, and AHUPM\*
```bash
[0]          [1]            [2]                       [3]                                [4]                      [5]
[Executable] [Threshold(%)] [Utility Data Path(.txt)] [Transaction Data File Path(.txt)] [Error Tolerance Factor] [Output File]
```

For IUOIL−, HUOMIL−, PULM, DUOCA\*−, and PIDUL\*
```bash
[0]          [1]            [2]                       [3]                                [4]
[Executable] [Threshold(%)] [Utility Data Path(.txt)] [Transaction Data File Path(.txt)] [Output File]
```

3. Next, the file name and the parameters of each dataset are as follows:

|  Dataset      | Database Size         | Number of Items | Average Transaction Length |
| ------------- | --------------------- | --------------- | -------------------------- |
| Accidents     | 340,183               | 468             | 33.8                       |
| Chess         | 3,196                 | 75              | 37.0                       |
| Mushroom      | 8,124                 | 119             | 23.0                       |
| Kosarak       | 990,002               | 41,270          | 8.1                        |
| AEP           | 19,735                | 130             | 26.0                       |
| AQ            | 9,326                 | 130             | 11.3                       |
| OnlineRetail  | 530,104               | 7,918           | 6.8                        |
| PAMAP         | 1,000,000             | 82              | 23.9                       |
| PowerC        | 1,040,000             | 125             | 7.0                        |
| T10I4DxK      | 200,000–1,000,000     | 100             | 10.0                       |
| TxI4D1000K    | 1,000,000             | 1,000           | 20.0–50.0                  |

The datasets can be found at https://drive.google.com/file/d/1SSPjZG-OuBxB05tvTi75Tf3xk0jiI6-m/view?usp=drive_link.

4. For example
```bash
AIUT 4.0 .\Data\utilAEP.txt .\Data\AEP.txt 0.1 out.txt
```
will run AIUT on AEP, with the threshold set at minimum utility : 4.0% and error tolerance factor : 0.1
```bash
IUOIL- 11.0 .\Data\utilMushroom.txt .\Data\Mushroom.txt out.txt
```
will run IUOIL− on Mushroom, with the threshold set at minimum utility : 11.0%

5. The output directory "/out" is required for writing result patterns for all algorithms.
