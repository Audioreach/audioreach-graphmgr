lib_LTLIBRARIES      = libagmclient.la
libagmclient_la_CPPFLAGS = -I $(top_srcdir)/service/inc/public -DAGM_USE_SYSLOG
libagmclient_la_CPPFLAGS += -I $(top_srcdir)/service/inc/public/agm
libagmclient_la_CPPFLAGS += $(GLIB_CFLAGS)
if USE_G_STR_FUNC
libagmclient_la_CPPFLAGS += -Dstrlcpy=g_strlcpy -Dstrlcat=g_strlcat
endif
libagmclient_ladir = $(libdir)
libagmclient_la_LDFLAGS = -ldl -lrt -shared -avoid-version
libagmclient_la_SOURCES = src/agm_client_wrapper_dbus.cpp
libagmclient_la_LDFLAGS += $(GLIB_LIBS) -lgobject-2.0 -lgio-2.0
