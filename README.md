# Molecular_Trajectory_Analysis
M.Tech_FirstSemester_Project

A. Prerequisites

You must have Scala v2.11.12 Spark v2.4.4
You must have sbt installed

B. Steps of Installation

1.Change your directory to Project Directory “MTA”
2.Compile Project using command “sbt compile”
3.Build JAR of Project using command “sbt package”
4.You can find the JAR file in “target” directory inside the project directory
5.Use this JAR to run modules

C. How to run Modules

1 Reading Please use a different JAR for this module path of JAR : /ppr.gp2/C3/read.jar Run the following command: spark-submit 
–class api.pdb_df –master yarn –deploy-mode cluster –num-executors –executor-cores –driver-memory –executor-memory 20g 
– conf spark.driver.maxResultSize=20g

2 Auto Image Run the following command: spark-submit –class api.autoImageMaster –master yarn –deploy-mode cluster –numexecutors
–executor-cores –driver-memory –executor-memory 20g –conf spark.driver.maxResultSize=20g

3 PDB Generation It gets generated in Auto Image Module itself

4 Masking Run the following command: spark-submit –class api.maskMasterf –master yarn –deploy-mode cluster –num-executors –executor-cores 
–driver-memory –executor-memory 20g – conf spark.driver.maxResultSize=20g

5 Average Structure Run the following command: spark-submit –class api.avgMaster –master yarn –deploy-mode cluster –num-executors
–executor-cores –driver-memory –executor-memory 20g – conf spark.driver.maxResultSize=20g

6 Distance Run the following command: spark-submit –class api.distanceMaster –master yarn –deploy-mode cluster –numexecutors
–executor-cores –driver-memory –executor-memory 20g –conf spark.driver.maxResultSize=20g

7 Angle Run the following command: spark-submit –class api.angleMaster –master yarn –deploy-mode cluster –num-executors 
–executor-cores –driver-memory –executor-memory 20g – conf spark.driver.maxResultSize=20g

8 RMSD Run the following command: spark-submit –class api.RmsdMasterAtom –master yarn –deploy-mode cluster – num-executors 
–executor-cores –driver-memory –executormemory 20g –conf spark.driver.maxResultSize=20g

9 Residue-Wise RMSD Run the following command: spark-submit –class api.RmsdMasterRes –master yarn –deploy-mode cluster –numexecutors 
–executor-cores –driver-memory –executor-memory 20g –conf spark.driver.maxResultSize=20g

10 Dihedral Run the following command: spark-submit –class api.dihedralMaster –master yarn –deploy-mode cluster –numexecutors 
–executor-cores –driver-memory –executor-memory 20g –conf spark.driver.maxResultSize=20g

11 Hydrogen Bond Run the following command: spark-submit –class api.HBondMaster –master yarn –deploy-mode cluster –numexecutors
–executor-cores –driver-memory –executor-memory 20g –conf spark.driver.maxResultSize=20g
