EXTRA_DIST = Cargo.toml \
	src/main.rs \
	$(null)

EXTRA_PROGRAMS = target/@CARGO_TARGET_DIR@/rustskel
target_@CARGO_TARGET_DIR@_rustskel_SOURCES =
all-local:
	cargo build --release
clean-local:
	-cargo clean
install-exec-local:
	$(MKDIR_P) $(DESTDIR)$(bindir)
	$(INSTALL) -c -m 755 target/@CARGO_TARGET_DIR@/rustskel $(DESTDIR)$(bindir)

DISTCLEANFILES =                                \
	$(null)

