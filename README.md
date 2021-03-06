      # Memory-Allocator, university project
      
  The program makes a simulation of a memory allocation system.
  
  The program receive commands for allocating, altering, displaying, and releasing memory, and output the results of each command.
  
  The program implements a number of working operations with arena (arena = a succession of N bytes), which will be launched by the commands it receives at the entrance. Each command is given on one line, and the results are displayed immediately.
  
  
  Commands format : 
  
  		1. INITIALIZE <N> 
			The command initializes the arena(assigns an N bytes area).

		2. FINALIZE
			The command releases the allocated memory.

		3. DUMP
			The command displays the entire memory map, byte byte.

		4. ALLOC <SIZE>
			The command allocate SIZE bytes of memory in the arena.

		5. FREE <INDEX>
			The command releases the memory block whose data sections start at position INDEX in the arena.

		6. FILL <INDEX> <SIZE> <VALUE> 
			The command sets SIZE consecutives bytes from arena, start at INDEX index and fill them with VALUE value.

		7.  SHOW <INFO>
			The command displays statistical information about the status of the arena.
			INFO can be one of the fallowing:
				- FREE
					Number of the free bytes in the arena is displayed.
				- USAGE
					Number of the usage bytes in the arena, efficiency and fragmentation are displayed.
				- ALLOCATIONS
					Free zones and allocated areas are displayed.

	Program testing is done automatically by running the check.sh script.
	There is a folder (_tests) that contains basic, random and advanced tests. Random tests will be generated every time when the check.sh script is run. The check.sh script compares the result of each test with the corresponding reference file from _tests folder. For each test, the commands are read from corresponding input file from same folder.
	The goal of the cs.py script is to identify places in the code that may be in non-compliance with google style.
	The generator.py file is used to generate multiple random memory allocation requests.
	
