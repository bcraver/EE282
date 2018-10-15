###Homework 2

1. After several months of waiting in anticipation, Ryan finally received news that he can begin analysis on his RNA-seq data. After logging onto the HPC, what command should Ryan type to view his main directories?  

	

	**Answer: clinicaltrial[ , c(2:3)]** or **clinicaltrial[ , c("weight","height")]**  #Answer Key: Include matrix name followed by single brackets. The weight and height columns (2:3) are indicated by ,c(2:3) or defined by their character names. 
	

3. Ryan just finished writing a script, “script.sh” under his "myfirstproject" directory (which is also currently only readable to the user). Ryan will share his script with a collaborator but only wants the collaborator to _read_ and _execute_ the script. Using octal permissions, how will Ryan share his script?  
 
	  $ chmod 755 script.sh** #Answer Key: 755 allows all to read and execute but only the user can write   
	     
  **$ chmod 755 myfirstproject**  #Answer Key: 755 will allow the parent directory "myfirstproject" to be readable and executable to all. The parent directories must be readable and executable in order for the script to be executable. 