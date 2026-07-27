TOP = ..
include $(TOP)/configure/CONFIG

export EPICSDBBUILDER

install: builder_path.py

builder_path.py: builder.py $(TOP)/configure/CONFIG_SITE epicsdbbuilder venv
	.venv/bin/python3 $< >$@

epicsdbbuilder: venv
	.venv/bin/pip install epicsdbbuilder==1.5

venv:
	$(PYTHON) -m venv .venv

clean:
	rm -f builder_path.py *.pyc

.PHONY: install clean
.DELETE_ON_ERROR: builder_path.py
