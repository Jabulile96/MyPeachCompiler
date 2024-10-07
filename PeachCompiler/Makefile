/*****************************************************************************************
                                        Makefile

This file is necessary for linking all the contibuting files to our C compiler. 
The files that are being connected are:

1. main.c
2. compiler.c
3. cprocess.c
4. lexer.c
5. token.c
6. lex_process.c
7. parser.c
8. node.c
9. scope.c
10. symresolver.c
11. array.c
12. expressionable.c
13. datatype.c
14. buffer.c


***********************************************************************************************/
# List of object files to be created
OBJECTS=
OBJECTS= ./build/compiler.o ./build/cprocess.o ./build/helpers/buffer.o ./build/helpers/vector.o

# Include directories for header files (-I flag)
INCLUDES= -I./

# The 'all' target - this is the default target that will be run if no other target is specified.
# It compiles 'main.c' and links it with the object files to create the 'main' executable.
all: ${OBJECTS}
	gcc main.c ${INCLUDES} ${OBJECTS} -g -o ./main 

# Rule to create './build/compiler.o' from './compiler.c'
# It compiles compiler.c into an object file with debugging info included (-g).
./build/compiler.o: ./compiler.c
	gcc compiler.c ${INCLUDES} -o ./build/compiler.o -g -c

./build/cprocess.o: ./cprocess.c
	gcc cprocess.c ${INCLUDES} -o ./build/cprocess.o -g -c

./build/lexer.o: ./lexer.c
	gcc lexer.c ${INCLUDES} -o ./build/lexer.o -g -c

./build/token.o: ./token.c
	gcc token.c ${INCLUDES} -o ./build/token.o -g -c

./build/lex_process.o: ./lex_process.c
	gcc lex_process.c ${INCLUDES} -o ./build/lex_process.o -g -c

./build/parser.o: ./parser.c
	gcc parser.c ${INCLUDES} -o ./build/parser.o -g -c

./build/node.o: ./node.c
	gcc node.c ${INCLUDES} -o ./build/node.o -g -c

./build/scope.o: ./scope.c
	gcc scope.c ${INCLUDES} -o ./build/scope.o -g -c

./build/symresolver.o: ./symresolver.c
	gcc symresolver.c ${INCLUDES} -o ./build/symresolver.o -g -c

./build/array.o: ./array.c
	gcc array.c ${INCLUDES} -o ./build/array.o -g -c

./build/expressionable.o: ./expressionable.c
	gcc expressionable.c ${INCLUDES} -o ./build/expressionable.o -g -c

./build/datatype.o: ./datatype.c
	gcc datatype.c ${INCLUDES} -o ./build/datatype.o -g -c



./build/helpers/buffer.o: ./helpers/buffer.c
	gcc ./helpers/buffer.c ${INCLUDES} -o ./build/helpers/buffer.o -g -c  # Generate buffer.o


./build/helpers/vector.o: ./helpers/vector.c
	gcc ./helpers/vector.c ${INCLUDES} -o ./build/helpers/vector.o -g -c  # Generate vector.o

# 'clean' target - removes the main executable and all object files.
# This is used for cleaning up the directory to allow for a fresh build.
clean:
	rm ./main  # Remove the 'main' executable
	rm -rf ${OBJECTS}  # Remove all object files specified in the OBJECTS variable
