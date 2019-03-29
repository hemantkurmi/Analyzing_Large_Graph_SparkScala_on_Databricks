Project objectives:

Eliminate any duplicate rows.
Filter the graph such that only nodes containing an edge weight >= 5 are preserved.  
Analyze the graph to find the nodes with the highest weighted-in-degree, weighted-out-degree, and weighted-total-degree using DataFrame operations.
Download a new DataFrame to q2output.csv containing your analysis (schema provided below).

We will analyze bitcoinotc.csv using Spark and Scala on the Databricks platform.  This graph is a who-trusts-whom network of people who trade using Bitcoin on a platform called Bitcoin OTC. The dataset has three columns in the following format - Source Node, Target Node, Edge Weight.


Notes 

If two or more nodes have the same weighted-out-degree, report the one with the lowest node id

If two or more nodes have the same weighted-in-degree, report the one with the lowest node id

If two or more nodes have the same weighted-total-degree, report the one with the lowest node id


Create a dataframe to store your results using the following schema:


Three columns, named: 'v', 'd', 'c' where:


v : vertex id


d : weighted-degree value (an integer value. one row with highest weighted-in-degree, a row with highest weighted-out-degree and a row with highest weighted-total-degree )


c : category of weighted-degree, containing one of three string values:

                                                'i' : weighted-in-degree

                                                'o' : weighted-out-degree                                                

                                                't' : weighted-total-degree

                                               

Your output can be downloaded as a .csv file or copied to a .csv file, as long as it meets the following requirements:


Your output shall contain exactly 4 rows.  (1 header row + 3 data rows)
The header row shall be of format v, d, c and must be the first row.
Your output shall contain exactly the column order specified.
The order of rows does not matter.


A correct output.csv for the input file would look like:

v,d,c

4,15,i

2,20,o

2,30,t

