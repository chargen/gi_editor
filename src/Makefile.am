include $(top_srcdir)/common/common.am

bin_PROGRAMS = read_midi sysex_explorer translator midi2jacksync studio_explorer

read_midi_SOURCES = read_midi.c
read_midi_LDADD = $(top_srcdir)/libgieditor/libgieditor.la \
		  $(top_srcdir)/common/libcommon.la

sysex_explorer_SOURCES = sysex_explorer.c
sysex_explorer_LDADD = $(top_srcdir)/libgieditor/libgieditor.la \
		  $(top_srcdir)/common/libcommon.la \
		  $(NCURSES_LIBS) $(PANEL_LIBS) $(FORM_LIBS) $(MENU_LIBS)
sysex_explorer_CFLAGS = $(NCURSES_CFLAGS)

studio_explorer_SOURCES = studio_explorer.c
studio_explorer_LDADD = $(top_srcdir)/libgieditor/libgieditor.la \
		  $(top_srcdir)/common/libcommon.la \
		  $(NCURSES_LIBS) $(PANEL_LIBS) $(FORM_LIBS) $(MENU_LIBS)
studio_explorer_CFLAGS = $(NCURSES_CFLAGS) -D_GNU_SOURCE -Wno-unused-result

translator_SOURCES = translator.c
translator_LDADD = $(top_srcdir)/libgieditor/libgieditor.la \
		  $(top_srcdir)/common/libcommon.la
translator_CFLAGS = $(JACK_CFLAGS)

midi2jacksync_SOURCES = midi2jacksync.c
midi2jacksync_LDADD = $(top_srcdir)/common/libcommon.la $(JACK_LIBS) \
		      $(top_srcdir)/avr/libavr.la -lm
midi2jacksync_CFLAGS = $(JACK_CFLAGS)

EXTRA_DIST = sysex_explorer.h korgnano.c
