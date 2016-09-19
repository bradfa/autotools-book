all: jupiter

check: all
	./jupiter | grep "Hello from .*jupiter!"
	@echo "*** ALL TESTS PASSED ***"

jupiter: main.c
	gcc -g -O0 -o $@ main.c

clean:
	-rm jupiter

install:
	install -d $(prefix)/bin
	install -m 0755 jupiter $(prefix)/bin

uninstall:
	-rm $(prefix)/bin/jupiter

.PHONY: all clean install uninstall
