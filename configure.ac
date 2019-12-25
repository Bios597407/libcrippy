AC_PREREQ(2.59)
AC_INIT(libcrippy-1.0, 1.0)
AM_CONFIG_HEADER(config.h)

# Checks for programs.
AM_PROG_LIBTOOL
AC_PROG_INSTALL
AC_PROG_MAKE_SET

AC_CANONICAL_SYSTEM
AM_INIT_AUTOMAKE(-Wall)

AM_PROG_CC_C_O
AC_LANG_C

AC_HEADER_STDC
AC_CONFIG_MACRO_DIR([m4])

# Checks the platform.
AC_MSG_CHECKING([whether to enable WIN32 specific flags])
case "$host_os" in
*mingw*)
        win32=true
        AC_MSG_RESULT([yes])
	AC_CHECK_TOOL(WINDRES, windres)
  ;;
*)
        win32=false
        AC_MSG_RESULT([no])
  ;;
esac
AM_CONDITIONAL(WIN32, test x$win32 = xtrue)

# Checks for libraries.
PKG_CHECK_MODULES(libplist, libplist >= 1.0)

AC_CONFIG_FILES(Makefile src/Makefile include/Makefile libcrippy-1.0.pc)
AC_OUTPUT
