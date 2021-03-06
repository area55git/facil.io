## System Requirements

The `facil.io` library requires Linux / BSD / macOS for proper operation. This is specifically due to the `evio.h` (evented IO) library and it's polling system.

Also, some of the file name resolution schemes (i.e., the one used for the HTTP static file service) also assume a POSIX system.

## Library Requirements

The `facil.io` library in this folder requires the `fiobj` library for parts of it's operations.

Specifically:

- The `websockets.h` extension uses the `fiobj` library for caching network data and the upgrade process.
- The `http.h` extension uses the `fiobj` library for authoring network packets and handling some network data.
- The `fio_cli.h` extension uses the `fiobj` library to manage it's inner data structures.
- The `fio2resp.h` is a translation unit between RESP (Redis) objects and `fiobj` objects (facio.io objects). By it's nature, it requires the `fiobj` library.

