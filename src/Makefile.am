INCLUDES =						\
	-DGNOMELOCALEDIR=\""$(datadir)/locale"\" 	\
	-DGETTEXT_PACKAGE=\""file-roller"\" 	\
	-I$(top_srcdir)					\
	-I$(top_builddir)

nemo_extensiondir=$(NEMO_EXTENSION_DIR)

nemo_extension_LTLIBRARIES=libnemo-engrampa.la

libnemo_engrampa_la_CFLAGS = 	                \
	-DDATADIR=\"$(datadir)\"					    \
	-DEMBLEMDIR=\"$(EMBLEM_DIR)\"					\
	-Wall                                           \
	$(WARN_CFLAGS)                                  \
	$(DISABLE_DEPRECATED_CFLAGS)					\
	$(NEMO_CFLAGS)                              \
	$(GLIB_CFLAGS)

if DEBUG
libnemo_engrampa_la_CFLAGS += -DND_DEBUG
else
libnemo_engrampa_la_CFLAGS += -DG_DISABLE_ASSERT -DG_DISABLE_CHECKS
endif

libnemo_engrampa_la_SOURCES = \
	engrampa-module.c       \
	nemo-engrampa.h       \
	nemo-engrampa.c

libnemo_engrampa_la_LDFLAGS = -module -avoid-version
libnemo_engrampa_la_LIBADD  = $(NEMO_LIBS) $(GLIB_LIBS)
