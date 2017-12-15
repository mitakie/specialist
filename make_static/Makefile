.PHONY : all clean dependencies

all : test

LIBS:=-L. -lhello

test : main.o libhello.a
	gcc -o $@ $< $(LIBS)

libhello.a : hello.o goodbye.o
	ar cr $@ $^

%.o : %.c
	gcc -c $<

clean : 
	rm -f test dependencies lib*.a *.o *~

dependencies :
	gcc -MM *.c >$@

include dependencies
