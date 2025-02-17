---
layout: talk
active: bob2015
title: Introduction to Riak
speaker: Christopher Meiklejohn
portrait: meiklejohn.jpg
time: 14:00-15:30
type: Tutorial
language: english
head: 2015
---

Riak is a highly-available, fault-tolerant, distributed
Dynamo-inspired key-value store.  Riak's primary focus is never losing
writes; whether this be sorting multiple values under concurrent
operations to the same key, or accepting writes in event of a network
partition.  During this session we will provide a brief tutorial on
how Riak works, and then explore the various APIs of which Riak
provides for building applications on top of.

### Preparations

For the tutorial, you should have a C compiler, and Erlang R16B02.

Here are detailed instructions:

[`http://docs.basho.com/riak/latest/ops/building/installing/erlang/`](http://docs.basho.com/riak/latest/ops/building/installing/erlang/)

Note: This is the same preparation as for the [Webmachine
tutorial](meiklejohn.html), and is also sufficient preparation
for the [Erlang tutorial](rehfeld.html).

### Christopher Meiklejohn

Christopher Meiklejohn is a Senior Software Engineer with Basho
Technologies, Inc. and a graduate student in the College of Computing
at Georgia Tech. Christopher is also a contributing member of the
European research project, SyncFree.
