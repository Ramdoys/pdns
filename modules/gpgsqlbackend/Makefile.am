AM_CPPFLAGS += $(PGSQL_CFLAGS) \
	$(LIBCRYPTO_INCLUDES)
pkglib_LTLIBRARIES = libgpgsqlbackend.la

EXTRA_DIST = \
	OBJECTFILES \
	OBJECTLIBS

dist_doc_DATA = \
	schema.pgsql.sql \
	nodnssec-3.x_to_3.4.0_schema.pgsql.sql \
	dnssec-3.x_to_3.4.0_schema.pgsql.sql \
	3.4.0_to_4.1.0_schema.pgsql.sql \
	4.1.0_to_4.2.0_schema.pgsql.sql \
	4.2.0_to_4.3.0_schema.pgsql.sql \
	4.3.0_to_4.7.0_schema.pgsql.sql

libgpgsqlbackend_la_SOURCES = \
	gpgsqlbackend.cc gpgsqlbackend.hh \
	spgsql.cc spgsql.hh

if GPGSQLBACKEND_DYNMODULE
libgpgsqlbackend_la_LDFLAGS = -module -avoid-version
else
libgpgsqlbackend_la_LDFLAGS = -static -avoid-version
endif
libgpgsqlbackend_la_LIBADD = $(PGSQL_LIBS)
