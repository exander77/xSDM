#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.62])
AC_INIT([xsdm], [0.2.0])
AC_CONFIG_SRCDIR([src/main.h])
AM_INIT_AUTOMAKE([subdir-objects])
AC_OUTPUT(Makefile src/Makefile tests/Makefile)
# AC_CONFIG_HEADERS([config.h])
PKG_CHECK_MODULES([CHECK], [check >= 0.9.4])

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC

# Checks for libraries.
AC_CHECK_LIB([z], [inflate],, [
         echo "Zlib is required for this program"
         exit -1])

AC_CHECK_LIB([mcrypt], [mcrypt_module_open],, [
         echo "Libmcrypt is required for this program"
         exit -1])

# Checks for header files.
AC_CHECK_HEADERS([stdint.h stdlib.h string.h errno.h stdio.h libgen.h zlib.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_CHECK_FUNCS([strstr strtoul])

AC_OUTPUT
