Meson bug showcase

```shell
$ rm -r build_rpi; meson setup build_rpi --cross-file=./rpi.cross
The Meson build system
Version: 1.6.1
Source dir: /tmp/meson_protobuf_bug
Build dir: /tmp/meson_protobuf_bug/build_rpi
Build type: cross build
Project name: my_project
Project version: undefined
C++ compiler for the host machine: /usr/bin/arm-linux-gnueabihf-g++ (gcc 11.4.0 "arm-linux-gnueabihf-g++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
C++ linker for the host machine: /usr/bin/arm-linux-gnueabihf-g++ ld.bfd 2.38
C++ compiler for the build machine: ccache c++ (gcc 11.4.0 "c++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
C++ linker for the build machine: c++ ld.bfd 2.38
Build machine cpu family: x86_64
Build machine cpu: x86_64
Host machine cpu family: arm
Host machine cpu: armv7l
Target machine cpu family: arm
Target machine cpu: armv7l

Executing subproject protobuf

protobuf| WARNING: Failed to load Cargo.lock: Could not find an implementation of tomllib, nor toml2json
protobuf| Project name: protobuf
protobuf| Project version: 25.2
protobuf| C compiler for the host machine: /usr/bin/arm-linux-gnueabihf-gcc (gcc 11.4.0 "arm-linux-gnueabihf-gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
protobuf| C linker for the host machine: /usr/bin/arm-linux-gnueabihf-gcc ld.bfd 2.38
protobuf| C++ compiler for the host machine: /usr/bin/arm-linux-gnueabihf-g++ (gcc 11.4.0 "arm-linux-gnueabihf-g++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
protobuf| C++ linker for the host machine: /usr/bin/arm-linux-gnueabihf-g++ ld.bfd 2.38
protobuf| C compiler for the build machine: ccache cc (gcc 11.4.0 "cc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
protobuf| C linker for the build machine: cc ld.bfd 2.38
protobuf| C++ compiler for the build machine: ccache c++ (gcc 11.4.0 "c++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
protobuf| C++ linker for the build machine: c++ ld.bfd 2.38
protobuf| Found pkg-config: NO
protobuf| Found CMake: NO
protobuf| Run-time dependency absl_string_view found: NO (tried pkgconfig and cmake)
protobuf| Looking for a fallback subproject for the dependency absl_string_view

Executing subproject protobuf:abseil-cpp

abseil-cpp| Project name: abseil-cpp
abseil-cpp| Project version: 20240722.0
abseil-cpp| C++ compiler for the host machine: /usr/bin/arm-linux-gnueabihf-g++ (gcc 11.4.0 "arm-linux-gnueabihf-g++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
abseil-cpp| C++ linker for the host machine: /usr/bin/arm-linux-gnueabihf-g++ ld.bfd 2.38
abseil-cpp| C++ compiler for the build machine: ccache c++ (gcc 11.4.0 "c++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0")
abseil-cpp| C++ linker for the build machine: c++ ld.bfd 2.38
abseil-cpp| Compiler for C++ supports arguments /DNOMINMAX: NO
abseil-cpp| Compiler for C++ supports arguments -Wno-sign-compare: YES
abseil-cpp| Compiler for C++ supports arguments -Wno-gcc-compat: NO
abseil-cpp| Checking for size of "void*" : 4
abseil-cpp| Compiler for C++ supports arguments -mfpu=neon: YES
abseil-cpp| Checking if "atomic builtins" : links: YES
abseil-cpp| Run-time dependency threads found: YES
abseil-cpp| Run-time dependency appleframeworks found: NO (tried framework)
abseil-cpp| Build targets in project: 15
abseil-cpp| Subproject abseil-cpp finished.

protobuf| Dependency absl_string_view from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_base from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_cord from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_die_if_null from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_hash from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_log from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_log_internal_check_op from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_log_internal_message from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_numeric from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_raw_hash_set from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_status from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_statusor from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_str_format from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_strings from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_synchronization from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency threads found: YES unknown (cached)
protobuf| Library dbghelp found: NO
protobuf| Program python3 found: YES (/home/user/tools/venv_meson/bin/python3)
protobuf| Dependency absl_log_initialize from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency threads found: YES unknown (cached)
protobuf| Dependency absl_base from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_cord from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_die_if_null from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_hash from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_log from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_log_internal_check_op from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_log_internal_message from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_numeric from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_raw_hash_set from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_status from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_statusor from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_str_format from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_strings from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_synchronization from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Dependency absl_string_view from subproject subprojects/abseil-cpp-20240722.0 found: YES 20240722.0
protobuf| Build-time dependency threads found: YES
protobuf| Library dbghelp found: NO

subprojects/protobuf-25.2/src/meson.build:29:18: ERROR: Tried to tied to mix a host machine library ("absl_base") with a build machine target "protoc-native" This is not possible in a cross build.

A full log can be found at /tmp/meson_protobuf_bug/build_rpi/meson-logs/meson-log.txt
```