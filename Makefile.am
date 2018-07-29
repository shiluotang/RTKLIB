ACLOCAL_AMFLAGS = -I m4

AM_CPPFLAGS = -Wall -Wno-unused-but-set-variable -ansi -pedantic -I$(top_srcdir)/src -DTRACE
AM_CFLAGS	=
AM_CXXFLAGS	=
AM_FFLAGS	=
AM_FCFLAGS	=
AM_LDFLAGS	=

lib_LTLIBRARIES = librtklib.la libiers.la

noinst_PROGRAMS = rnx2rtcm str2str pos2kml convbin rnx2rtkp rtkrcv

librtklib_la_SOURCES = \
./src/convkml.c \
./src/convrnx.c \
./src/datum.c \
./src/download.c \
./src/ephemeris.c \
./src/geoid.c \
./src/ionex.c \
./src/lambda.c \
./src/options.c \
./src/pntpos.c \
./src/postpos.c \
./src/ppp_ar.c \
./src/ppp.c \
./src/preceph.c \
./src/qzslex.c \
./src/rcv/binex.c \
./src/rcv/crescent.c \
./src/rcv/gw10.c \
./src/rcv/javad.c \
./src/rcv/novatel.c \
./src/rcv/nvs.c \
./src/rcvraw.c \
./src/rcv/rcvlex.c \
./src/rcv/rt17.c \
./src/rcv/septentrio.c \
./src/rcv/skytraq.c \
./src/rcv/ss2.c \
./src/rcv/ublox.c \
./src/rinex.c \
./src/rtcm2.c \
./src/rtcm3.c \
./src/rtcm3e.c \
./src/rtcm.c \
./src/rtkcmn.c \
./src/rtkpos.c \
./src/rtksvr.c \
./src/sbas.c \
./src/solution.c \
./src/stream.c \
./src/streamsvr.c \
./src/tle.c

libiers_la_SOURCES = \
lib/iers/src/cal2jd.f \
lib/iers/src/dat.f \
lib/iers/src/dehanttideinel.f \
lib/iers/src/gmf.f \
lib/iers/src/gpt.f \
lib/iers/src/norm8.f \
lib/iers/src/sprod.f \
lib/iers/src/st1idiu.f \
lib/iers/src/st1isem.f \
lib/iers/src/st1l1.f \
lib/iers/src/step2diu.f \
lib/iers/src/step2lon.f \
lib/iers/src/vmf1.f \
lib/iers/src/vmf1_ht.f \
lib/iers/src/zero_vec8.f

rnx2rtcm_CPPFLAGS = $(AM_CPPFLAGS) -DENAGLO -DENAGAL -DENAQZS -DNFREQ=3 -DNEXOBS=3
rnx2rtcm_LDFLAGS = -lm
rnx2rtcm_SOURCES = \
./src/rinex.c \
./src/rtcm.c \
./src/rtcm2.c \
./src/rtcm3.c \
./src/rtcm3e.c \
./src/rtkcmn.c \
./util/rnx2rtcm/rnx2rtcm.c

# prevent "both compiled with and without libtool" failure.
str2str_CPPFLAGS = $(AM_CPPFLAGS) -DENAGLO -DENAGAL -DENAQZS -DENACMP -DNFREQ=3 -DNEXOBS=3
str2str_LDFLAGS = -lm -lrt -lpthread
str2str_SOURCES = \
./app/str2str/str2str.c \
./src/geoid.c \
./src/preceph.c \
./src/rcv/binex.c \
./src/rcv/crescent.c \
./src/rcv/gw10.c \
./src/rcv/javad.c \
./src/rcv/novatel.c \
./src/rcv/nvs.c \
./src/rcv/rt17.c \
./src/rcv/skytraq.c \
./src/rcv/ss2.c \
./src/rcv/ublox.c \
./src/rcvraw.c \
./src/rtcm.c \
./src/rtcm2.c \
./src/rtcm3.c \
./src/rtcm3e.c \
./src/rtkcmn.c \
./src/sbas.c \
./src/solution.c \
./src/stream.c \
./src/streamsvr.c

pos2kml_CPPFLAGS = $(AM_CPPFLAGS)
pos2kml_LDFLAGS = -lm -lrt
pos2kml_SOURCES = \
./app/pos2kml/pos2kml.c \
./src/convkml.c \
./src/geoid.c \
./src/preceph.c \
./src/rtkcmn.c \
./src/solution.c

convbin_CPPFLAGS = $(AM_CPPFLAGS) -DENAGLO -DENAGAL -DENAQZS -DENACMP -DNFREQ=6 -DNEXOBS=3
convbin_LDFLAGS = -lm -lrt
convbin_SOURCES = \
./app/convbin/convbin.c \
./src/convrnx.c \
./src/ephemeris.c \
./src/ionex.c \
./src/pntpos.c \
./src/preceph.c \
./src/qzslex.c \
./src/rcv/binex.c \
./src/rcv/crescent.c \
./src/rcv/gw10.c \
./src/rcv/javad.c \
./src/rcv/novatel.c \
./src/rcv/nvs.c \
./src/rcv/rt17.c \
./src/rcv/skytraq.c \
./src/rcv/ss2.c \
./src/rcv/ublox.c \
./src/rcvraw.c \
./src/rinex.c \
./src/rtcm.c \
./src/rtcm2.c \
./src/rtcm3.c \
./src/rtcm3e.c \
./src/rtkcmn.c \
./src/sbas.c

rnx2rtkp_CPPFLAGS = $(AM_CPPFLAGS) -DENAGLO -DENAQZS -DENAGAL -DNFREQ=3
rnx2rtkp_LDFLAGS = -lm -lrt
rnx2rtkp_SOURCES = \
./app/rnx2rtkp/rnx2rtkp.c \
./src/ephemeris.c \
./src/geoid.c \
./src/ionex.c \
./src/lambda.c \
./src/options.c \
./src/pntpos.c \
./src/postpos.c \
./src/ppp.c \
./src/ppp_ar.c \
./src/preceph.c \
./src/qzslex.c \
./src/rinex.c \
./src/rtcm.c \
./src/rtcm2.c \
./src/rtcm3.c \
./src/rtcm3e.c \
./src/rtkcmn.c \
./src/rtkpos.c \
./src/sbas.c \
./src/solution.c

rtkrcv_CPPFLAGS = $(AM_CPPFLAGS) -DENAGLO -DENAQZS -DENACMP -DNFREQ=3
rtkrcv_LDFLAGS = -lm -lrt -lpthread
rtkrcv_SOURCES = \
./app/rtkrcv/rtkrcv.c \
./app/rtkrcv/vt.c \
./src/ephemeris.c \
./src/geoid.c \
./src/ionex.c \
./src/lambda.c \
./src/options.c \
./src/pntpos.c \
./src/ppp.c \
./src/ppp_ar.c \
./src/preceph.c \
./src/qzslex.c \
./src/rcv/binex.c \
./src/rcv/crescent.c \
./src/rcv/gw10.c \
./src/rcv/javad.c \
./src/rcv/novatel.c \
./src/rcv/nvs.c \
./src/rcv/rt17.c \
./src/rcv/skytraq.c \
./src/rcv/ss2.c \
./src/rcv/ublox.c \
./src/rinex.c \
./src/rtcm.c \
./src/rtcm2.c \
./src/rtcm3.c \
./src/rtcm3e.c \
./src/rtkcmn.c \
./src/rtkpos.c \
./src/rtksvr.c \
./src/sbas.c \
./src/solution.c \
./src/stream.c \
./src/rcvraw.c
