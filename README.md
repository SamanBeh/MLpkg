# MLpkg
A small and ready to use package for supervised machine learning tasks that we have initially developed it for the CpACpP project (http://cbb1.ut.ac.ir/CpACpP/Index)


**USAGE:**

**python** **main.py** **-i** input_file_path
               **-l** label_col_name
               **-o** output_root_dir
               [**-c** col_name_to_delete]
               [**-s** cv_splits]
               [**-r** n_cv_repeats]
               [**-j** n_jobs]
               [**-p** output_name_postfix]
               [**-m** model_names]
               [**-s** 0 or 1]

**Options:**

-h  (--help) --> Shows these instructions :)

-i  (--input) --> The input file path

-l  (--labelcol) --> The labels' column name

-o  (--out) --> (default="") The output root directory

-c  (--colsdel) --> (default="") Column names you want to be removed from the
                    training data. e.g. sample_name1,sample_name2
										
-k  (--kfold) --> (default=10) The value of  k  for k-fold cross validation.
                    i.e. The number of folds
										
-r  (--repeats) --> (default=10) The number of iterations for the cross validation stage

-j  (--jobs) --> (default=8) Number of threads for running modles

-p  (--postfix) --> (default="") The postfix for output file names

-m  (--models) --> (defaults=rf,svm,xgb) Models that you want to build and test.
                    divide names with ','. e.g.  rf,svm,xgb,knn,gnb
                    Available machines:
                        RF  = Random Forest
                        SVM = Support Vector Machine
                        XGB = eXtreme Gradient Boosting
                        KNN = K-Nearest Neighbors
                        GNB = Gussian Naive Bayes
												
-s  (--save) --> (default=0) Set it to 1 if you want to save your model as a
                    joblib file.
										
-t  (--testsplit) --> (default=0.25) The test split size

-x  (--stanscale) --> (default=0) Set it to 1 if you want to standardize features

