vaapidir = $(pluginsdir)/vaapi

libvlc_vaapi_instance_la_SOURCES = hw/vaapi/instance.c hw/vaapi/vlc_vaapi.h
libvlc_vaapi_instance_la_CFLAGS = $(LIBVA_CFLAGS)
libvlc_vaapi_instance_la_LIBADD = $(LIBVA_LIBS) $(LIBPTHREAD)
libvlc_vaapi_instance_la_LDFLAGS = -no-undefined	\
				   -version-info 0:0:0

libvaapi_chroma_plugin_la_SOURCES = hw/vaapi/chroma.c hw/vaapi/vlc_vaapi.c hw/vaapi/vlc_vaapi.h	\
				    video_chroma/copy.c video_chroma/copy.h
libvaapi_chroma_plugin_la_CFLAGS = $(AM_CFLAGS) $(LIBVA_CFLAGS)
libvaapi_chroma_plugin_la_LIBADD = $(AM_LIBADD) $(LIBVA_LIBS) libvlc_vaapi_instance.la

if HAVE_VAAPI
vaapi_LTLIBRARIES = libvlc_vaapi_instance.la	\
		    libvaapi_chroma_plugin.la
endif
