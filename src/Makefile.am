AM_CFLAGS = -I$(top_srcdir)/include $(libplist_CFLAGS)
AM_LDFLAGS = $(libplist_LIBS)

lib_LTLIBRARIES = libcrippy-1.0.la
libcrippy_1_0_la_CFLAGS = $(AM_CFLAGS)
libcrippy_1_0_la_LDFLAGS = $(AM_LDFLAGS)

if WIN32
libcrippy_1_0_la_LDFLAGS = -all-static -static-libgcc $(AM_LDFLAGS)
endif

libcrippy_1_0_la_SOURCES = \
						libcrippy.c \
						file.c \
						directory.c \
						architecture.c \
						fuzz.c

