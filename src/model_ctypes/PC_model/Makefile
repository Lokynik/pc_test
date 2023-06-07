CC=gcc
CFLAGS=-Wall -fPIC -c
EXECUTABLE=ina.so
SOURCES=ina.c main.c
OBJECTS=$(SOURCES:.c=.o)

all:clean o $(EXECUTABLE)
$(EXECUTABLE):$(OBJECTS)
	$(CC) -shared $(OBJECTS) -o $(EXECUTABLE) -lm  -L../SDL/lib -lsundials_cvode 

o:ina.c
	$(CC) $(CFLAGS) -I../SDL/include $(SOURCES) $(SOURCES)

clean:
	rm -rf $(OBJECTS) $(EXECUTABLE)
