SUBDIRS = src 3rd-party include rtos etc m4 cmake build

EXTRA_DIST = \
			minigui.pc.in \
            GNUmakefile makefile.ng makefile.msvc rules.make \
            Version INSTALL LICENSE \
            README.md RELEASE-NOTES.md \
            LICENSE-POLICY-en.md LICENSE-POLICY-zh.md 

# The directory where the include files will be installed
libminiguiincludedir = $(includedir)/minigui

# Which header files to install
libminiguiinclude_HEADERS = mgconfig.h

docs:
	doxygen Doxyfile.procs Doxyfile.ths Doxyfile.sa

dist-nolicense: dist
	./clean_license.sh $(DIST_ARCHIVES)

dist:
distcheck-nolicense:dist-nolicense distcheck

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = minigui.pc

