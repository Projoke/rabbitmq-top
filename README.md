# RabbitMQ Top Plugin

Adds UNIX top-like information on the Erlang VM to the management plugin.

Screenshots: http://imgur.com/a/BjVOP

## Supported RabbitMQ Versions

This plugin is compatible with RabbitMQ `3.4.0` and later versions.

## Usage

Sort by process ID, memory use or reductions/sec (an approximate
measure of CPU use).

Click on the process description (e.g. "my queue") to see that
object's management view.

Click on the process ID (e.g. "&lt;0.3423.0&gt;") to see some more
Erlang-ish process details, including the current stacktrace.

## HTTP API

You can drive the HTTP API yourself. It installs into the management plugin's API; you should understand that first. Once you do, the additional paths look like:

    /api/top/<node-name>

List of processes. Takes similar query string parameters to other
lists, `sort`, `sort_reverse` and `columns`. Sorting is quite
important as it currently hard-codes returning the top 20 processes.

    /api/process/<pid>

Individual process details.

## Downloading

You can download a pre-built binary of this plugin from [RabbitMQ Community plugins page](http://www.rabbitmq.com/community-plugins.html).

## Building from Source

You can build and install it like any other plugin (see
[the plugin development guide](http://www.rabbitmq.com/plugin-development.html)).

## License and Copyright

(c) Pivotal Software Inc, 2007—2016

Released under the same license as RabbitMQ.
