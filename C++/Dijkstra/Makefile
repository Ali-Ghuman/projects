dijkstra.exe: dijkstra.o graph.o heap.o hash.o
	g++ -o dijkstra.exe dijkstra.o graph.o heap.o hash.o

dijkstra.o: dijkstra.cpp graph.h heap.h hash.h
	g++ -c dijkstra.cpp

graph.o: graph.cpp graph.h heap.h hash.h
	g++ -c graph.cpp

heap.o: heap.cpp heap.h hash.h
	g++ -c heap.cpp

hash.o: hash.cpp hash.h
	g++ -c hash.cpp

debug:
	g++ -g -o dijkstraDebug.exe dijkstra.cpp graph.cpp heap.cpp hash.cpp

clean:
	rm -f *.exe *.o *.stackdump *~

backup:
	test -d backups || mkdir backups
	cp *.cpp backups
	cp *.h backups
	cp Makefile backups