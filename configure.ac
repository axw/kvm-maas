# -*- Autoconf -*-

AC_PREREQ([2.69])

AC_INIT([kvm-maas], [0.1], [aim@frobware.com])
AC_CONFIG_AUX_DIR([config])
AC_CANONICAL_TARGET
AC_CANONICAL_HOST
AC_CONFIG_MACRO_DIR([config])
AC_CONFIG_MACRO_DIRS([m4])
AM_INIT_AUTOMAKE([foreign dist-bzip2 no-dist-gzip])
AM_MAINTAINER_MODE([enable])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

# Checks for programs.

AC_CHECK_PROG(PYTHON2_CHECK,python2,yes)
if test x"$PYTHON2_CHECK" != x"yes"; then
    AC_MSG_ERROR([Please install package python2.])
fi

AC_CHECK_PROG(XMLSTARLET_CHECK,xmlstarlet,yes)
if test x"$XMLSTARLET_CHECK" != x"yes"; then
    AC_MSG_ERROR([Please install package xmlstarlet.])
fi

AC_CHECK_PROG(VIRSH_CHECK,virsh,yes)
if test x"$VIRSH_CHECK" != x"yes"; then
    AC_MSG_ERROR([Please install package libvirt-bin.])
fi

AC_CHECK_PROG(VIRT_INSTALL_CHECK,virt-install,yes)
if test x"$VIRT_INSTALL_CHECK" != x"yes"; then
    AC_MSG_ERROR([Please install package virtinst.])
fi

AC_CHECK_PROG(MAASCLI_CHECK,maas,yes)
if test x"$MAASCLI_CHECK" != x"yes"; then
    AC_MSG_ERROR([Please install package maas-cli.])
fi

# Checks for libraries.

AC_PYTHON_MODULE(libvirt)
if test x"$HAVE_PYMOD_libvirt" != x"yes"; then
    AC_MSG_ERROR([Please install package python-libvirt.])
fi

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
