## mirage-flow-rawlink -- Expose rawlink interfoaces as MirageOS flows

Allow to use rawlink interfaces as MirageOS flows.

[![docs](https://img.shields.io/badge/doc-online-blue.svg)](https://mirage.github.io/mirage-flow-rawlink/mirage-flow-rawlink)

An example:

```ocaml
  Lwt_rawlink.open_link "eth0" >>= fun rawlink ->
  Mirage_flow_lwt.read rawlink >>= function
  | Ok (`Data buf) ->
  ...
```