include $(top_srcdir)/modules.am

SUBDIRS = \
	. \
	captureplan

noinst_HEADERS = protocol_tcp.h localapi.h uthash.h parser_tls.h define.h decryption.h
#
protocol_tcp_la_SOURCES  = protocol_tcp.c localapi.c parser_tls.c decryption.c
protocol_tcp_la_CFLAGS   = -Wall ${MODULE_CFLAGS}
protocol_tcp_la_LDFLAGS  = -I/usr/include/openssl -module -avoid-version
protocol_tcp_la_LIBADD   = ${PTHREAD_LIBS} ${EXPAT_LIBS} ${GCRYPT_LIBS} ${CRYPTO_LIBS} -lm
protocol_tcp_laconfdir   = $(confdir)
protocol_tcp_laconf_DATA = $(top_srcdir)/conf/protocol_tcp.xml

mod_LTLIBRARIES = protocol_tcp.la
