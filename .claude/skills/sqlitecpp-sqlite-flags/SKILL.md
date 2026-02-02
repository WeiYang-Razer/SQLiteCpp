---
name: sqlitecpp-sqlite-flags
description: SQLiteCpp and sqlite3 feature flags. Use when enabling or disabling SQLite features in CMake or Meson builds.
---

# SQLiteCpp and SQLite Flags

## Core SQLiteCpp options (CMake)
- `SQLITECPP_INTERNAL_SQLITE` (ON): build bundled sqlite3.
- `SQLITECPP_USE_ASAN` (OFF): address sanitizer.
- `SQLITECPP_USE_GCOV` (OFF): coverage.
- `SQLITECPP_DISABLE_STD_FILESYSTEM` (OFF): disable std::filesystem.
- `SQLITECPP_DISABLE_EXPANDED_SQL` (OFF): disable sqlite3_expanded_sql.

## SQLite feature flags (CMake and Meson)
- `SQLITE_ENABLE_COLUMN_METADATA` (ON): enable `getColumnOriginName()`.
- `SQLITE_ENABLE_ASSERT_HANDLER` (OFF): enable custom assert handler.
- `SQLITE_HAS_CODEC` (OFF): enable codec API (SQLCipher).
- `SQLITE_USE_LEGACY_STRUCT` (OFF): legacy `sqlite3_value`.
- `SQLITE_OMIT_LOAD_EXTENSION` (OFF): disable load_extension.
- `SQLITE_ENABLE_RTREE` (OFF): enable RTree (internal sqlite3).
- `SQLITE_ENABLE_DBSTAT_VTAB` (OFF): enable DBSTAT (internal sqlite3).

## DLL build flags (Windows)
- `BUILD_SHARED_LIBS=ON` adds `SQLITECPP_COMPILE_DLL` and `SQLITECPP_DLL_EXPORT`.

## Usage notes
- Column metadata requires sqlite3 built with `SQLITE_ENABLE_COLUMN_METADATA`.
- External sqlite3 may not support load_extension on macOS.
