ifndef verbose
.SILENT:
endif

# default target: Compile and run main.c if no program is specified
default: main

# Generic rule to compile and run any c program
%: %.c
	gcc -o $@ $<
	./$@

# Purge rule to remove all compiled binaries, with a message
purge:
	FILES="$(wildcard $(basename $(wildcard *.c)))"; \
	if [ -n "$$FILES" ]; then \
		echo "Purging: $$FILES"; \
		rm -f $$FILES; \
	else \
		echo "No compiled files to purge."; \
	fi
