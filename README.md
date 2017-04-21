# TIC1project
TIC1 Project  
  
Fully argument version to easy and fast testing without changing source code    
Argument list with default values in []: (no need to use directed order)  
Project.exe (Program name...of course)  
-i \<input hash> [ahoj]  
-b \<biteSize> [32]    
-p \<probability of false positive> [0.005/5E-3]     
-c \<capacity of array(in M)> [10]  
-t \<thread number> [cpu threads]  
-l (logging) [false]  
-m \<multiplier of filter size>  
-n \<modulo of writing hash> [10] (tested just with 10/100/1000, should work with others like 20,50, but need to test)
-r (ringMode) [false]

Ring mode - used for testing/searching for lenght collision ring, need to use when you set input first collision hash
     
full example: Project.exe -i ahoj -b 56 -p 0.005(5E-3) -c 100 -n 10000 -m 4 -n -10 -t 4 -l (-r)   
  
Logging:   
every 10th M of filter IO operations - console and logFile   
every 5th K of array operations - console and logFile   

USAGE Table:  
  
Bit lenght - capacity - saving step  
  
<=36b	      10M	      1 000  
40-48	     100M	     10 000  
52-56	   1,000M     100 000  
60-64	  50,000M	    100 000  
68-76	 500,000M	  1 000 000  
80    ????????M 	??????????  

