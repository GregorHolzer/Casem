# Casem

The goal of this project is to reimplement the [Cirrina](https://github.com/CollaborativeStateMachines/Cirrina/) Runtime in Go. 
This new Runtime (Casem) should provide all features of the Cirrina Runtime as well as a programatic API to develop and compile StateMachines. 
Therefore this project is made up of multiple milestones:

## Development of Casem

The initial step is to port the Cirrina Runtime from Kotlin to Go with all it's existing features and the possibility to run StateMachines written in the CSML language via pkl files. 

### Comparison Cirrina (Kotlin) vs Casem (Go)

After Casem is developed a performance comparison between Cirrina and Casem would be neccessary. 
For this purpose there already exist a couple of benchmarks and use case examples at [Cirrina-Examples](https://github.com/CollaborativeStateMachines/Cirrina-Examples). 
This examples are written in pkl files an can therefore be used for Cirrina and Casem as is.

## Programmatic API for Casem

The next step would be to create a programmatic API for Casem to develop and run StateMachines. This would enable to embed the StateMachines into the final binary instead of parsing them as pkl files on application startup.

### Comparison Casem (Pkl) vs Casem (Naitive)

Finally a performance comparison between StateMachines that are implemented in 

* pkl files (parsed at startup of Casem runtime)
* programmatic API (embedded in binary)

Therefore again the benchmarks and use cases from the Cirrina-Examples can be used.


