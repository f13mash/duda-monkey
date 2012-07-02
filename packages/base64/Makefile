CC      = arm-linux-androideabi-gcc
CFLAGS  =  -O2 -Wall -fvisibility=hidden
LDFLAGS = 
DEFS    =  -DTRACE -DACCEPT_GENERIC
INCDIR  = ../../../../src/include -I../../src
OBJECTS = duda_package.o base64.o
SOURCES = duda_package.c base64.c

all: ../base64.dpkg

../base64.dpkg: $(OBJECTS)
	$(CC) $(CFLAGS) $(LDFLAGS) $(DEFS) -shared -Wl -o $@ $^ -lc

.c.o: $(SOURCES)
	$(CC) $(CFLAGS) $(DEFS) -I$(INCDIR) -fPIC -c $<

clean:
	rm -rf *~ *.o
