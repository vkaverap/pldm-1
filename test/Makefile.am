AM_CPPFLAGS = -I$(top_srcdir)

TESTS = $(check_PROGRAMS)

check_PROGRAMS = \
	libpldm_base_test \
	libpldmresponder_base_test

test_cppflags = \
	-Igtest \
	$(GTEST_CPPFLAGS) \
	$(AM_CPPFLAGS)

test_cxxflags = \
	$(PTHREAD_CFLAGS)

test_ldflags = \
	-lgtest_main \
	-lgtest \
	$(PTHREAD_LIBS) \
	$(OESDK_TESTCASE_FLAGS)

libpldm_base_test_CPPFLAGS = $(test_cppflags)
libpldm_base_test_CXXFLAGS = $(test_cxxflags)
libpldm_base_test_LDFLAGS = $(test_ldflags)
libpldm_base_test_LDADD = $(top_builddir)/libpldm/base.o
libpldm_base_test_SOURCES = libpldm_base_test.cpp

libpldmresponder_base_test_CPPFLAGS = $(test_cppflags)
libpldmresponder_base_test_CXXFLAGS = $(test_cxxflags)
libpldmresponder_base_test_LDFLAGS = $(test_ldflags)
libpldmresponder_base_test_LDADD = \
	$(top_builddir)/libpldm/base.o \
	$(top_builddir)/libpldmresponder/base.o
libpldmresponder_base_test_SOURCES = libpldmresponder_base_test.cpp
