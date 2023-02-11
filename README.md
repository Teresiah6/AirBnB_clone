## Description 🏠                                                                                                                  
                                                                                                                                   
AirBnB is a complete web application, integrating database storage, a back-end AA                                                  
PI, and front-end interfacing in a clone of AirBnB.                                                                                
                                                                                                                                   
The project currently only implements the back-end console.                                                                        
                                                                                                                                   
## Classes 🆑                                                                                                                      
                                                                                                                                   
HolbertonBnB utilizes the following classes:                                                                                       
                                                                                                                                   
## Storage 🛄                                                                                                                      
                                                                                                                                   
The above classes are handled by the abstracted storage engine defined in the Fii                                                  
leStorage class.                                                                                                                   
                                                                                                                                   
Every time the backend is initialized, HolbertonBnB instantiates an instance of                                                    
FileStorage called storage. The storage object is loaded/re-loaded from any class                                                  
s instances stored in the JSON file file.json. As class instances are created, uu                                                  
pdated, or deleted, the storage object is used to register corresponding changess                                                  
 in the file.json. 

## Console 💻                                                                                                                      
                                                                                                                                   
The console is a command line interpreter that permits management of the backendd                                                  
 of HolbertonBnB. It can be used to handle and manipulate all classes utilized bb                                                  
y the application (achieved by calls on the storage object defined above).                                                         
                                                                                                                                   
#### Using the Console                                                                                                             
                                                                                                                                   
The HolbertonBnB console can be run both interactively and non-interactively. Too                                                  
 run the console in non-interactive mode, pipe any command(s) into an execution                                                    
of the file console.py at the command line.   

$ echo "help" | ./console.py                                                                                                   
                                                                                                                                   
    (hbnb)                                                                                                                         
                                                                                                                                   
    Documented commands (type help <topic>):                                                                                       
                                                                                                                                   
    ========================================                                                                                       
                                                                                                                                   
    EOF  all  count  create  destroy  help  quit  show  update                                                                     
                                                                                                                                   
    (hbnb)                                                                                                                         
                                                                                                                                   
    $                                                                                                                              
                                                                                                                                   
                                                                                                                                   
Alternatively, to use the HolbertonBnB console in interactive mode, run the filee                                                  
 console.py by itself:    

`$ ./console.py`                                                                                                                   
                                                                                                                                   
While running in interactive mode, the console displays a prompt for input:                                                        
                                                                                                                                   
    $ ./console.py                                                                                                                 
                                                                                                                                   
    (hbnb)                                                                                                                         
                                                                                                                                   
To quit the console, enter the command quit, or input an EOF signal (ctrl-D).                                                      
                                                                                                                                   
                                                                                                                                   
                                                                                                                                   
    $ ./console.py                                                                                                                 
                                                                                                                                   
    (hbnb) quit                                                                                                                    
                                                                                                                                   
    $               

or                                                                                                                                 
                                                                                                                                   
                                                                                                                                   
                                                                                                                                   
    $ ./console.py                                                                                                                 
                                                                                                                                   
    (hbnb) EOF                                                                                                                     
                                                                                                                                   
    $                                                                                                                              
                                                                                                                                   
                                                                                                                                   
                                                                                                                                   
## console Commands                                                                                                                
                                                                                                                                   
The AirBnB console supports the following commands:                                                                                
                                                    
- create                                                                                                                           
                                                                                                                                   
 - Usage: create <class>                                                                                                           
                                                                                                                                   
                                                                                                                                   
                                                                                                                                   
Creates a new instance of a given class. The class' ID is printed and the instann                                                  
ce is saved to the file file.json.  

                                                                                                                                  
    $ ./console.py                                                                                                                 
                                                                                                                                   
    (hbnb) create BaseModel                                                                                                        
                                                                                                                                   
    119be863-6fe5-437e-a180-b9892e8746b8                                                                                           
                                                                                                                                   
    (hbnb) quit                                                                                                                    
                                                                                                                                   
    $ cat file.json ; echo ""                                                                                                      
                                                                                                                                   
    {"BaseModel.119be863-6fe5-437e-a180-b9892e8746b8": {"updated_at": "2019-02-11                                                  
7T21:30:42.215277", "created_at": "2019-02-17T21:30:42.215277", "__class__": "Baa                                                  
seModel", "id": "119be863-6fe5-437e-a180-b9892e8746b8"}}                                                                           
                                                          
