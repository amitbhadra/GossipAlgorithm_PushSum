
# PROJECT 2 - DOS
<br/> 
Written using F# and Akka

Team Members:
 - Amit Asish Bhadra (66494087)
 - Rishab Aryan Das (05369273)

Instructions to run:

 - unzip project2.zip
 - unzip project2-bonus.zip

	To run gossip: <br/> 
		cd project2 <br/> 
		dotnet fsi --langversion:preview Proj2.fsx <num_nodes> <topology> gossip <br/> 
	Eg: <br/> 
		dotnet fsi --langversion:preview Proj2.fsx 100 2D gossip <br/> 
<br/> 
	To run Push sum: <br/> 
		cd project2 <br/> 
		dotnet fsi --langversion:preview Proj2.fsx <num_nodes> <topology> push-sum <br/> 
	Eg: <br/> 
		dotnet fsi --langversion:preview Proj2.fsx 2000 imp2D push-sum <br/> 
<br/> 
	To run Push sum(multi messages): <br/> 
		cd project2 <br/> 
		dotnet fsi --langversion:preview Proj2-multiplePS.fsx <num_nodes> <topology> push-sum <br/> 
	Eg: <br/> 
		dotnet fsi --langversion:preview Proj2-multiplePS.fsx 2000 imp2D push-sum <br/> 
<br/> 
	To run Bonus Gossip: <br/> 
		cd project2-bonus <br/> 
		dotnet fsi --langversion:preview Proj2-bonus.fsx <num_nodes> <topology> gossip <br/> 
	Eg: <br/> 
		dotnet fsi --langversion:preview Proj2-bonus.fsx 2000 imp2D gossip <br/> 


What is working:
 - For gossip we have implemented our network for upto 20000 nodes and reported upto 10000
 - For Push sum we have experimented both with single and multiple messages upto 20000 nodes and reported upto 10000. As expected, line doesn't converge for the single active message way for over 1000 nodes. Using multiple active messages we have solved this but even then the convergence takes a considerably long time.
 - For bonus, implemented Failure Model for Gossip Protocol

Order of convergence:
 - Gossip: Full < Imp2D < 2D < Line
 - Push Sum: Full < Imp2D < 2D < Line

Largest Network that is converging:

 - Gossip:
 	- Line: 20000
	- 2D: 50000
	- Full: 100000
	- Imp2D: 60000

 - Push Sum(multi):
 	- Line: 20000
  	- 2D: 50000
  	- Full: 100000
  	- Imp2D: 70000
