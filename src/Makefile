all: jupiter

check: all
	./jupiter | grep "Hello from .*jupiter!"
	@echo "*** ALL TESTS PASSED ***"

jupiter: main.c
	gcc -g -O0 -o $@ main.c

clean:
	-rm jupiter

install:
	install -d $(DESTDIR)$(bindir)
	install -m 0755 jupiter $(DESTDIR)$(bindir)

uninstall:
	-rm $(DESTDIR)$(prefix)/bin/jupiter

.PHONY: all clean install uninstall
