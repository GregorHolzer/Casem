# Casem

The goal of this project is to reimplement the [**Cirrina**](https://github.com/CollaborativeStateMachines/Cirrina/) runtime in Go. 
The new runtime, **Casem** should extend the existing the functionality of Cirrina by providing a programmatic API to develop state machines enabling it to:

* Run state machines from .pkl files
* Compile state machines from the API to native binaries
* Compile state machines from the API to WebAssembly

## Development of Casem

The first step is to port the Cirrina Runtime from Kotlin to Go with all existing features and the possibility to run state machines via `.pkl files. 

### Comparison: Cirrina (.pkl) vs Casem (.pkl)

Once Casem is developed a performance comparison between Cirrina and Casem will be necessary. 
A set of well-known benchmarks is already available at [Cirrina-Examples](https://github.com/CollaborativeStateMachines/Cirrina-Examples). 
These benchmarks are written in .pkl files and can therefore be used unchanged for both Cirrina and Casem, providing a fair comparison between the two runtimes.

## Programmatic API for Casem

The next step is to create Casem’s programmatic API, which allows developers to define state machines in Go and compile them to either native binaries or WebAssembly.

### Comparison: Casem (.pkl) vs Casem (API)

At last a performance comparison between running state machines with casem that are implemented via:

* .pkl files
* the programmatic API

For this evaluation the benchmarks of the Cirrina-Examples can be used again. 

## Conclusion

Finally, there will be multiple ways to run and develop state machines based on the exact requirements:

<table>
  <tr>
    <th></th>
    <th style="text-align:center" colspan="2">Cirrina</th>
    <th style="text-align:center" colspan="2">Casem</th>
  </tr>
  <tr>
    <td>Language</td>
    <td style="text-align:center" colspan="2">Kotlin</td>
    <td style="text-align:center" colspan="2">Go</td>
  </tr>
  <tr>
    <td>Execution</td>
    <td style="text-align:center">JVM</td>
    <td style="text-align:center">Docker + JVM</td>
    <td style="text-align:center">Naitive Binary</td>
    <td style="text-align:center">WASM Runtime</td>
  </tr>
  <tr>
    <td>State Machines</td>
    <td style="text-align:center" colspan="2">.pkl</td>
    <td style="text-align:center">.pkl</td>
    <td style="text-align:center">API</td>
  </tr>
  <tr>
    <td >Containerization</td>
    <td style="text-align:center" colspan="2">Docker</td>
    <td style="text-align:center" colspan="2">WASM Runtime</td>
  </tr>
</table>
