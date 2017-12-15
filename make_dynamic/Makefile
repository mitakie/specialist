.PHONY : all clean dependencies

all : test

LIBS:=-L. -lhello

test : main.o libhello.so
	gcc -o $@ $< $(LIBS)

libhello.so : hello.o goodbye.o
	gcc -shared -o $@ $^

%.o : %.c
	gcc -c -fPIC $<

clean : 
	rm -f test dependencies lib*.a *.o *~

dependencies :
	gcc -MM *.c >$@

include dependencies
