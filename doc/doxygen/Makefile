default: full
all: full

%.tag: %.doxy
	doxygen $<

FULL = \
	documentation.doxy

full: $(FULL:.doxy=.tag)
	$(foreach FILE,$(FULL),doxygen $(FILE);)

clean:
	-rm -rf $(FULL:.doxy=)
	-rm -rf *.tag
	-rm -rf *.db
