+++
title = "Protocol Buffers"
weight = 5
toc_hide = "true"
description = "Protocol Buffers are language-neutral, platform-neutral extensible mechanisms for serializing structured data."
type = "docs"
no_list = "true"
+++

<!--* css: "//depot/includes/suppress-nav.css" *-->

<style>
.row .highlight {
    margin-top: 2rem;
    margin-right: 0;
    margin-bottom: 0;
    margin-left: 0;
    padding: 0;
}
</style>

<div class="row">
<div class="col-md">

```proto
message Person {
  optional string name = 1;
  optional int32 id = 2;
  optional string email = 3;
}
```

<p class="caption">A proto definition.</>
</div>
<div class="col-md">

```java
// Java code
Person john = Person.newBuilder()
    .setId(1234)
    .setName("John Doe")
    .setEmail("jdoe@example.com")
    .build();
output = new FileOutputStream(args[0]);
john.writeTo(output);

```

<p class="caption">Using a generated class to persist data.</p>
</div>
<div class="col-md">

```cpp
// C++ code
Person john;
fstream input(argv[1],
    ios::in | ios::binary);
john.ParseFromIstream(&input);
id = john.id();
name = john.name();
email = john.email();

```

<p class="caption">Using a generated class to parse persisted data.</p>
</div>
</div>
<div class="row">
<div class="col-md">

## What Are Protocol Buffers?

Protocol buffers are Google's language-neutral, platform-neutral, extensible
mechanism for serializing structured data – think XML, but smaller, faster, and
simpler. You define how you want your data to be structured once, and then you
can use special generated source code to easily write and read your structured
data to and from a variety of data streams and using a variety of languages.

</div>
<div class="col-md">

## Pick Your Favorite Language

Protocol buffers support generated code in C++, C#, Dart, Go, Java,
Kotlin,
Objective-C, Python, and Ruby. With proto3, you can also work with PHP.

</div>
<div class="col-md">

## How Do I Start?

<ol>

  <li>
    <a href="https://github.com/protocolbuffers/protobuf#protobuf-compiler-installation">Download
    and install</a> the protocol buffer compiler.
  </li>

  <li>
    Read the
    <a href="/overview">overview</a>.
  </li>
  <li>
    Try the <a href="/getting-started">tutorial</a> for your
    chosen language.
  </li>
</ol>

</div>
</div>
