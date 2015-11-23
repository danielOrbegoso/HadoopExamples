    Program Name: Sudoku

    Source code : /org/apache/hadoop/examples/dancing/ (yarn jar hadoop-mapreduce-examples.jar sudoku) /*You need to execute this code and to be in
			the folder /usr/lib/hadoop-mapreduce first*/

    Description: Hadoop has provides an example jar file for test purposes. In this jar file there is an example to solve sudoku problems.
		

    Usage:  We need to send an input file ,the one we need to create as we showed in the sample experiment. It has to be always with a par number of columns and 
	    rows and if we want to create and output file to keep the output information, we just add it at the end. (It has to be in the same directory)	
    Options:

    Sample Experiments:

	   1st. We need to send to this example and input file

		To use this example we need to make an input file for the sudoku problem. In this file each sudoku cell can be either a number or ‘?’ with spaces as 			separators.Like this one:
			
		8 5 ? 3 9 ? ? ? ?
		? ? 2 ? ? ? ? ? ?
		? ? 6 ? 1 ? ? ? 2
		? ? 4 ? ? 3 ? 5 9
		? ? 8 9 ? 1 4 ? ?
		3 2 ? 4 ? ? 8 ? ?
		9 ? ? ? 8 ? 5 ? ?
		? ? ? ? ? ? 2 ? ?
		? ? ? ? 4 5 ? 7 8

		File : prueba
		I have created this file in my Desktop.
	   2nd. Hadoop Part

		Now we need to save this input file in our local directory. And give this input to hadoop example jar. 

		[cloudera@quickstart hadoop-mapreduce]$ yarn jar hadoop-mapreduce-examples.jar sudoku /home/cloudera/Desktop/prueba /user/cloudera/dataSudoku

		/*To execute this code you need to be in this folder first /usr/lib/hadoop-mapreduce*/

		with this command we will send to the sudoku de file we have created and we will keep the output in the file dataSudoku.

		Solving prueba
		8 5 1 3 9 2 6 4 7
		4 3 2 6 7 8 1 9 5
		7 9 6 5 1 4 3 8 2
		6 1 4 8 2 3 7 5 9
		5 7 8 9 6 1 4 2 3
		3 2 9 4 5 7 8 1 6
		9 4 7 2 8 6 5 3 1
		1 8 5 7 3 9 2 6 4
		2 6 3 1 4 5 9 7 8

		Found 1 solutions

		Hadoop give you the all possible solutions for the puzzle in a few seconds.( If there is more than one answer the time will be higher).
 		(Input and output must be in the same folder)
