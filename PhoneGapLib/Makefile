.SILENT: all phonegap-js submodules clean

SHELL = /bin/sh
CHMOD = chmod
CP = cp
MV = mv
NOOP = $(SHELL) -c true
RM_F = rm -f
RM_IR = rm -iR
RM_RF = rm -rf
TEST_F = test -f
TOUCH = touch
UMASK_NULL = umask 0
DEV_NULL = > /dev/null 2>&1
MKPATH = mkdir -p
CAT = cat
MAKE = make
OPEN = open
JAVA = java
ECHO = echo
ECHO_N = echo -n
PG_JS_CORE = javascripts/core
pgver = $(shell head -1 VERSION)
JAVASCRIPT_PATH = javascripts
PHONEGAP_JS_PATH = phonegap-js

all :: phonegap-js

phonegap-js: clean submodules
	$(MAKE) -C ${PHONEGAP_JS_PATH} ios
	$(MKPATH) ${JAVASCRIPT_PATH}
	$(CP) ${PHONEGAP_JS_PATH}/build/*.js ${JAVASCRIPT_PATH}

submodules:
	cd ../; git submodule update --init

clean:
	$(RM_RF) ${JAVASCRIPT_PATH}; \