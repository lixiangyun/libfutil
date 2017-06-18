#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT(helloworld, 1.0, linimbus@126.com)
AC_CONFIG_SRCDIR([src/helloworld.c])
AC_CONFIG_HEADERS([include/config.h])
AM_INIT_AUTOMAKE

AC_CONFIG_FILES([Makefile
src/Makefile])


# Checks for programs.
AC_PROG_CC

# Checks for libraries.
AC_CHECK_LIB([pthread], [pthread_rwlock_init])
AC_PROG_RANLIB
# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_OUTPUT
