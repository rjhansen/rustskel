AC_INIT([rustskel], m4_esyscmd([grep ^version Cargo.toml | awk '{print $3}' | tr -d '"' | tr -d "\n"]), [rob@hansen.engineering])
AM_INIT_AUTOMAKE([1.11 foreign no-dependencies no-dist-gzip dist-xz subdir-objects])

VERSION=$(grep ^version Cargo.toml | awk '{print $3}' | tr -d '"' | tr -d "\n")

AC_CHECK_PROG(CARGO, [cargo], [yes], [no])
AS_IF(test x$CARGO = xno,
    AC_MSG_ERROR([cargo is required])
)
AC_CHECK_PROG(RUSTC, [rustc], [yes], [no])
AS_IF(test x$RUSTC = xno,
    AC_MSG_ERROR([rustc is required])
)

CARGO_TARGET_DIR=release
AC_SUBST(CARGO_TARGET_DIR)
AC_SUBST(VERSION)
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
