## Process this file with automake to produce Makefile.in

AM_CFLAGS = \
	$(BLKID_CFLAGS) \
	$(EXT2FS_CFLAGS) \
	$(TRACEFS_CFLAGS) \
	$(TRACEEVENT_CFLAGS)

AM_CPPFLAGS = \
	-DLOCALEDIR="\"$(localedir)\"" \
	-I$(top_builddir) -I$(top_srcdir) -iquote$(builddir) -iquote$(srcdir) \
	-I$(top_srcdir)/intl


sbin_PROGRAMS = \
	ureadahead

ureadahead_SOURCES = \
	ureadahead.c \
	trace.c trace.h \
	pack.c pack.h \
	values.c values.h \
	logging.c logging.h
ureadahead_LDADD = \
	-lrt \
	$(BLKID_LIBS) \
	$(EXT2FS_LIBS) \
	$(LTLIBINTL) \
	$(TRACEEVENT_LIBS) \
	$(TRACEFS_LIBS)
ureadahead_LDFLAGS = \
	-pthread


clean-local:
	rm -f *.gcno *.gcda

maintainer-clean-local:
	rm -f *.gcov
