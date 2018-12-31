# Data-Cleaning

Cleaning the raw data file:

The cleaning involves extracting a substring from a string.

Divide the raw data file into two parts:
1. Eliminate all the rows containing RsID from the Name column and keep only the rows who do not contain RsID.
   e.g.- chr1-4657678_ilmnbot, MReverse_14566767_ilmnTOP keep this and remove GSA-rs4567778_ilmntop

2. Eliminate the rows which do not contain RsID in the Name column.
   e.g. - GSA-rs1234578.1,newrs345677_f2bt keep this and remove chr1-4657678_ilmnbot, MReverse_14566767_ilmnTOP

Now, merge the 1st part which doesn't conatin RsID with the mapping data file provided. 
This will give us the coreesponding RsID for a given text in the Name column.

After this, clean the extra characters associated with the RsID in the 2nd part. For this use the Cleaning.ipynb.
***Note--- In this 2nd part file, open the csv and replace all the '_' with '-'. Replace 'new' with 'new-'. Replace 'RS' with 'rs'.
           This has to be done otherwise some of the rows will be left blank.***

Merge both the parts together.
