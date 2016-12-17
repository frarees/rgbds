AC_PREREQ([2.68])
AC_INIT([rgbds], [0.2.4])

AC_CONFIG_SRCDIR([src/asm/main.c])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_AUX_DIR([build.scripts])

AM_INIT_AUTOMAKE([1.11 subdir-objects -Wall -Werror])
AC_CONFIG_FILES([Makefile])

AC_PROG_CC
AC_PROG_CC_C99

AC_PROG_YACC

AC_SEARCH_LIBS([cos],
	[m],
	[],
	[AC_MSG_ERROR(['m cannot be found (required by rgbasm)'])])

OLDLIBS=[$LIBS]
LIBS=
AC_SEARCH_LIBS([png_create_read_struct],
	[png png10 png12 png16],
	[],
	[AC_MSG_ERROR(['libpng cannot be found (required by rgbgfx)'])])
AC_SUBST([LIBPNG_LDFLAGS], [$LIBS])
LIBS=[$OLDLIBS]

AC_CHECK_HEADERS([png.h \
libpng/png.h \
libpng10/png.h \
libpng12/png.h \
libpng16/png.h],,,
[[#if HAVE_PNG_H
# include <png.h>
#endif
]])

AC_OUTPUT
