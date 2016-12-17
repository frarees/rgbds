AM_CPPFLAGS = -Iinclude -D_POSIX_C_SOURCE=200809L
AM_YFLAGS = -d

bin_PROGRAMS = rgbasm rgbfix rgblink rgbgfx

noinst_HEADERS = include

BUILT_SOURCES = src/asm/asmy.h

rgbasm_SOURCES = \
	src/extern/err.c \
	src/extern/reallocarray.c \
	src/extern/strlcat.c \
	src/extern/strlcpy.c \
	src/asm/asmy.y \
	src/asm/charmap.c \
	src/asm/fstack.c \
	src/asm/globlex.c \
	src/asm/lexer.c \
	src/asm/locallex.c \
	src/asm/main.c \
	src/asm/math.c \
	src/asm/output.c \
	src/asm/rpn.c \
	src/asm/symbol.c

rgbfix_SOURCES = \
	src/extern/err.c \
	src/fix/main.c

rgblink_SOURCES = \
	src/extern/err.c \
	src/link/assign.c \
	src/link/library.c \
	src/link/main.c \
	src/link/mapfile.c \
	src/link/object.c \
	src/link/output.c \
	src/link/patch.c \
	src/link/symbol.c

rgbgfx_SOURCES = \
	src/extern/err.c \
	src/gfx/gb.c \
	src/gfx/main.c \
	src/gfx/makepng.c

rgbgfx_LDFLAGS = $(LIBPNG_LDFLAGS)

dist_man_MANS = src/rgbds.7 src/asm/rgbasm.1 src/fix/rgbfix.1 src/gfx/rgbgfx.1 src/link/rgblink.1
