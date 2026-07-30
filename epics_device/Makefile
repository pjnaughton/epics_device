TOP = ..
include $(TOP)/configure/CONFIG

install: builder_path.py

builder_path.py: builder.py $(TOP)/configure/CONFIG_SITE
	.venv/bin/python3 $< >$@

clean:
	rm -f builder_path.py *.pyc

.PHONY: install clean
.DELETE_ON_ERROR: builder_path.py
