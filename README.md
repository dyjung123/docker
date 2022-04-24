# Macで Docker VMに screen commandを使って入ろうとしたら [screen is terminating] が出て Docker Desktopに入れない error回避法メモ

[出所](https://stackoverflow.com/questions/63445657/why-i-am-getting-screen-is-terminating-error-in-macos)

``` sh
docker run -it --privileged --pid=host debian nsenter -t 1 -m -u -n -i sh
```

OR

``` sh
docker run --rm -it --privileged --pid=host walkerlee/nsenter -t 1 -m -u -i -n sh
```
