####Homework 2

1a. After several months of waiting in anticipation, Ryan finally received news that he can begin analysis on his RNA-seq data. After logging onto the HPC, what command should Ryan type to view his main directories?  

	Answer: `$ ls or ll` #Answer Key: ls or ll lists the main directories
	
1b. Ryan saw that his practice RNAseq directory was still listed. How can Ryan remove the "practiceRNAseq" directory then make a new README.md file to document where he is saving the new RNA-seq data?

`$ rm practiceRNA seq`  
`$ touch README.md`  

#Answer Key: use rm to remove a directory. Use touch to create a new file if it doesn't already exist.  

### Q1 Comments:
Hi, although you did provide an example of ls or ll, you did not provide examples of touch, mv and rm. Please update Q1 so that it includes at least these operations. 
Thank you. :)
	
2. Ryan wants to subset the "clinicaltrial" matrix which consists of numerical indices listing patients age, weight and height in columns (columns 1-3, respectively) and patient names in rows. How would Ryan subset the clinicaltrial matrix to observe only patient weight and height?

	**Answer: `clinicaltrial[ , c(2:3)]** or **clinicaltrial[ , c("weight","height")]** `   
	#Answer Key: Include matrix name followed by single brackets. The weight and height columns (2:3) are indicated by ,c(2:3) or defined by their character names. 
	
### Q2 Comments:
You addressed the issue of matrices only using both index names and index numbers. You didn't address data frames. So, you took a bit of Q2.1 and a bit of Q2.2 and mixed them rather than choosing one of the two and answering it fully. Please demonstrate some concepts of dealing with dataframe columns.

3. Ryan just finished writing a script, “script.sh” under his "myfirstproject" directory (which is also currently only readable to the user). Ryan will share his script with a collaborator but only wants the collaborator to _read_ and _execute_ the script. Using octal permissions, how will Ryan share his script?  
 
	**Answer:  
	  `$ chmod 755 script.sh**`   #Answer Key: 755 allows all to read and execute but only the user can write   
	     
 ` **$ chmod 755 myfirstproject** ` #Answer Key: 755 will allow the parent directory "myfirstproject" to be readable and executable to all. The parent directories must be readable and executable in order for the script to be executable. 

### Question 3 Comments:
Question 3 was done correctly and allows executiong by not only the owner, but the group and all users, as you have specified. One thing to note though is that for real world applications the parent directory and all subsequent parent directories must have the 755 permission, otherwise the collaborator will not be able to access any of the subdirectories where read access has been denied. Just food for thought.

Also in general you can use "'''sh <myblock of code> '''" for adding script into your markdown file. The quotes do have to be the slanted ones though. i.e `
