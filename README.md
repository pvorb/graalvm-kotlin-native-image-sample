GraalVM & Kotlin `native-image` sample
======================================

## Prerequisites

- GraalVM needs to be installed and on $PATH

## Building

~~~
./mvnw package
~~~

## Running

~~~
target/graalvm-kotlin-native-image-sample-1.0.0
~~~

will print

~~~
Hello, world
~~~

## Startup time

~~~
time target/graalvm-kotlin-native-image-sample-1.0.0
Hello, world
target/graalvm-kotlin-native-image-sample-1.0.0  0.00s user 0.00s system 83% cpu 0.003 total
~~~

vs

~~~
time java -jar target/graalvm-kotlin-native-image-sample-1.0.0.jar
Hello, world
java -jar target/graalvm-kotlin-native-image-sample-1.0.0.jar  0.08s user 0.01s system 106% cpu 0.082 total
~~~

## Binary size

~~~
du -h target/graalvm-kotlin-native-image-sample-1.0.0
3.4M	target/graalvm-kotlin-native-image-sample-1.0.0
~~~
