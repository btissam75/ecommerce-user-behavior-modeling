# Dataset

This repository does not redistribute the Yoochoose / RecSys Challenge 2015 data.

Obtain the dataset from an authorized source and place the required files in a local, untracked directory. The notebooks expect the following source files:

```text
yoochoose-clicks.dat
yoochoose-buys.dat
```

The original notebooks use Google Drive paths similar to:

```text
/content/drive/MyDrive/proj_indiv/data/yoochoose-data/
```

Before execution, update the `CLICKS_PATH` and `BUYS_PATH` variables to match your environment.

Do not commit raw data, processed user-level exports, credentials, or private storage links. The repository `.gitignore` excludes common local data directories and dataset file patterns.

