SHELL=/bin/sh
DIRS = *

.PHONY: all
all:
	for d in $(DIRS); do\
		if [ -d $$d ]; then\
			($(MAKE) -C $$d)\
		fi;\
	done

.PHONY: spelling
spelling:
	for d in $(DIRS); do\
		if [ -d $$d ]; then\
		(cd $$d; $(MAKE) spelling );\
		fi;\
	done

.PHONY: distclean
distclean:
	@-rm -f *~
	for d in $(DIRS); do\
		if [ -d $$d ]; then\
		(cd $$d; $(MAKE) distclean );\
		fi;\
	done

.PHONY: clean
clean:
	@-rm -f *~
	for d in $(DIRS); do\
		if [ -d $$d ]; then\
		(cd $$d; $(MAKE) clean );\
		fi;\
	done
