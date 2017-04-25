# Hints for using ns3
###### Hint 1
- logging and assertions are only available in debug builds. 
- Recommended practice is to develop your scenario in debug mode, then conduct repetitive runs (for statistics or changing parameters) in optimized build profile.

```c++



####### Hint: multiple builds (deply & run?)
- work with multiple builds simultatiously?
- When you switch, Waf will only compile what it has to, instead of recompiling everything.

```bash
 ./waf configure --build-profile=debug --out=build/debug
```
###### Hint: program arguments
in the background, $s is replaced with name of the program (```<ns3-program>```). From that we can infer the correct use of a debugger.

```bash
$ ./waf --run <ns3-program> --command-template="%s <args>"
```


debugger ```gdb```
```bash
./waf --run=hello-simulator --command-template="gdb %s --args <args>"
```


###### Hint: convention for placement of binaries

```c++
function waff { CWD="$PWD"

```



# Concepts of ns3
- Node = basic computing device abstraction. Class ```Node```
