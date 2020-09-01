## Executor

The *Executor* is the working horse of the asynchronous processing. He pretty much represents the runtime that is able to continuously request the result of every `Future` until they return the `Ready` state. Registering a `Future` at the *Executor* to have the *Executor* to run the `Future` to completion is called *spawning*. As part of *spawning*, the `Future` is wrapped into a structure that allows proper handling of processing and re-spawning of pending futures. In Rust libraries this wrapper is typically called a *Task*.
