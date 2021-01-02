# stackoverflow-springbatchRestart
#Sample data
Jill,Doe
Joe,Doe
Gowri,Rakesh
Rakesh,Sahadevan
Madhav,Rakesh

#Execute the Job by giving "parameter1" in SpringBoot class 
  
-- First time All records are loaded
-- Again execute you will get error saying that 
   -- "A job instance already exists and is complete for parameters={file.input=parameter1}"

#Truncate the table Execute the Job by giving "parameter2" in SpringBoot class and remove delimitter from third row

Jill,Doe
Joe,Doe
GowriRakesh
Rakesh,Sahadevan
Madhav,Rakesh

# Two records will be loaded and You will get an error "Parsing error at line: 3 in resource=[class path resource [sample-data.csv]], input=[GowriRakesh]"
# Restart the job with same parameter and you will get same error "Parsing error at line: 3 in resource=[class path resource [sample-data.csv]], input=[GowriRakesh]"
# Correct the data you can see remaining 3 records were again loaded. Remaining data will be loaded starting from Gowri,Rakesh


