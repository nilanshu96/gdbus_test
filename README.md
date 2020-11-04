# Simple dbus server and client using GDBUS

## Compiling and running

compile
```shell
$ make gen
$ make
```

run
```shell
$ ./server
$ ./client
```

introspect and call using gdbus command line
```shell
$ gdbus introspect -e -d com.fatminmin -o /com/fatminmin/GDBUS
$ gdbus call -e -d com.fatminmin -o /com/fatminmin/GDBUS -m com.fatminmin.GDBUS.HelloWorld [your name]
```
gdbus-codegen call
```shell
$ gdbus-codegen --generate-c-code minminbus       \
                --c-namespace MinMinBus           \
                --interface-prefix com.fatminmin. \
                com.fatminmin.GDBUS.xml 
```
