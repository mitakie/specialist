.PHONE : all clean dependencies

all : test

test : main.o hello.o goodbye.o
	gcc -o $@ $^

%.o : %.c
	gcc -c $<

clean : 
	rm -f test dependencies *.o *~

dependencies :
	gcc -MM *.c >$@

include dependencies
