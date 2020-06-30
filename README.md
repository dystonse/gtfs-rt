# gtfs-rt

**This repository is a part of the multi-repository project `dystonse`. See the [main repository](https://github.com/dystonse/dystonse) for more information.**

_This project is forked from [barzamin/gtfs-rt](https://github.com/barzamin/gtfs-rt)._

## Original project
The original project combines the official `.proto` file for [GTFS realtime](https://developers.google.com/transit/gtfs-realtime) with [prost](https://github.com/danburkert/prost) to generate Rust types for GTFS-rt feeds.

## Fork Modification
This fork will add an extension for encoding probability distributions for delay predictions. 

The probability distributions are represented as [dystonse curves](https://github.com/dystonse/dystonse-curves).

We did not yet apply for an extension id, and are currently using `1023` until we do. This id is subject to change!

## Extension workaround
The general [documentation about GTFS-rt extensions](https://developers.google.com/transit/gtfs-realtime/guides/extensions) mandates the usage of [protobuf extensions](https://developers.google.com/protocol-buffers/docs/proto#extensions). Since prost currently does not support extensions, we use a [workaround](https://github.com/danburkert/prost/issues/100#issuecomment-390266699) from the related [Issue #100](https://github.com/danburkert/prost/issues/100).