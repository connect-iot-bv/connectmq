# ConnectMQ: Apache 2.0 MQTT Broker

> **ConnectMQ** is a fork of [VerneMQ](https://github.com/vernemq/vernemq) - built from source with **Apache 2.0 license only**, no proprietary EULA.

![Build Status](https://github.com/connect-iot-bv/connectmq/actions/workflows/release.yml/badge.svg)
## Key Differences from Upstream VerneMQ

- ✅ **Pure Apache 2.0** - No proprietary licensing or EULA restrictions
- ✅ **Multi-architecture** - Native AMD64 and ARM64 builds  
- ✅ **Built from source** - Full transparency, no precompiled binaries
- ✅ **Automated releases** - GitHub Actions build and release pipeline

## Quick Start

### Download Pre-built Binaries

```bash
# Download latest release for your architecture
wget https://github.com/connect-iot-bv/connectmq/releases/latest/download/connectmq-v*-linux-amd64.tar.gz
# or
wget https://github.com/connect-iot-bv/connectmq/releases/latest/download/connectmq-v*-linux-arm64.tar.gz

# Extract and run
tar -xzf connectmq-v*-linux-*.tar.gz
cd vernemq
bin/vernemq start
```

### System Requirements

- **Linux**: Ubuntu 20.04+, Debian 11+, RHEL 8+
- **Dependencies**: `libsnappy1v5` (install with `apt-get install libsnappy1v5`)
- **Architecture**: AMD64 (x86_64) or ARM64 (aarch64)

---

## About VerneMQ

ConnectMQ is built on **VerneMQ**, a high-performance, distributed MQTT message broker. It scales horizontally and vertically on commodity hardware to support a high number of concurrent publishers and consumers while maintaining low latency and fault tolerance.

**Original VerneMQ** is developed by the VerneMQ team and available at [github.com/vernemq/vernemq](https://github.com/vernemq/vernemq).

VerneMQ is an Apache2 licensed distributed [MQTT](http://www.mqtt.org) broker, developed in [Erlang](http://www.erlang.org).

MQTT used to stand for MQ Telemetry Transport, but it no longer is an
acronym. It is an extremely simple and lightweight publish/subscribe messaging
protocol, that was invented at IBM and Arcom (now Eurotech) to connect
restricted devices in low bandwidth, high-latency or unreliable networks.

VerneMQ implements the MQTT 3.1, 3.1.1 and 5.0 specifications. Currently the
following features are implemented and delivered as part of VerneMQ:

* QoS 0, QoS 1, QoS 2
* Basic Authentication and Authorization
* Bridge Support
* $SYS Tree for monitoring and reporting
* TLS (SSL) Encryption
* Websockets Support
* Cluster Support
* Logging (Console, Files, Syslog)
* Reporting to Graphite
* Extensible Plugin architecture
* Multiple Sessions per ClientId
* Session Balancing
* Shared subscriptions
* Message load regulation
* Message load shedding (for system protection)
* Offline Message Storage (based on LevelDB)
* Queue can handle messages FIFO or LIFO style.
* MongoDB auth & integration
* Redis auth & integration
* MySQL auth & integration
* PostgreSQL auth & integration
* CockroachDB auth & integration
* Memcached integration
* HTTP Webhooks
* PROXY Protocol v2
* Administration HTTP API
* Real-time MQTT session tracing
* Full multitenancy
* Cluster status web page

The following features are also applies to MQTT 5.0 clients:

* Enhanced authentication schemes (AUTH)
* Message expiration
* Last Will and Testament delay
* Shared subscriptions
* Request/response flow
* Topic aliases
* Flow control
* Subscription flags (Retain as Published, No Local, Retain Handling)
* Subscriber identifiers
* All property types are supported: user properties, reason strings, content types etc.

## Commercial Support. Binary Packages. Documentation

Below you'll find a basic introduction to building and starting VerneMQ. For
more information about the binary package installation, configuration, and
administration of VerneMQ, please visit our documentation at [VerneMQ
Documentation](https://docs.vernemq.com) or checkout the product page
[VerneMQ](https://vernemq.com) if you require more information on the available
commercial [support options](https://vernemq.com/services.html).

## VerneMQ Release Schedule

VerneMQ releases will be annonced based on bugfixes and features.

Usually a bugfix release will be cut between minor releases or
if there's an urgent bugfix pending.

Custom releases can be offered for commercial users.

## Quick Start

This section assumes that you have a copy of the VerneMQ source tree. To get
started, you need to first build VerneMQ.

### Building VerneMQ

Note: VerneMQ requires Erlang/OTP 25-27 and `libsnappy-dev` installed in your system. You'll also need a C compiler for Eleveldb. (on Debian, you install `build-essential`, as an example).

Assuming you have a working Erlang installation, building VerneMQ should be as
simple as:

```shell
$ cd $VERNEMQ
$ make rel
```

### Starting VerneMQ

Once you've successfully built VerneMQ, you can start the server with the following
commands:

```shell
$ cd $VERNEMQ/_build/default/rel/vernemq
$ bin/vernemq start
```

If VerneMQ is running it is possible to check the status on
`http://localhost:8888/status` and it should look something like:


<img src="https://i.imgur.com/XajYjtb.png" width="75%">

Note that the `$VERNEMQ/_build/default/rel/vernemq` directory is a complete,
self-contained instance of VerneMQ and Erlang. It is strongly suggested that you
move this directory outside the source tree if you plan to run a production
instance.

### Important links

* [VerneMQ Documentation](https://docs.vernemq.com)
* [![Google group : VerneMQ Users](https://img.shields.io/badge/Google%20Group-VerneMQ%20Users-blue.svg)](https://groups.google.com/forum/#!forum/vernemq-users)
* <a href="https://twitter.com/vernemq">
		<img
			alt="Twitter: VerneMQ"
			src="https://img.shields.io/twitter/follow/vernemq.svg?style=social"
			target="_blank"
		/>
	</a>

### Thank you to all our contributors!
[![contributors](https://contributors-img.web.app/image?repo=vernemq/vernemq)](https://github.com/vernemq/vernemq/graphs/contributors)
