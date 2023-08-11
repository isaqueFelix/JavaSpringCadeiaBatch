# Job2App

This sample serves two purposes:
- show how to create a simple Batch Job ([`job.go`](./job.go))
- how to have that Job call an Application running in the same project. This
  will use the private network within the project - meaning the private
  endpoint of the app, not a public-facing one.

When the Job is run, each instance will call the App 10 times. Which means
by setting the `array-indices` to a range of 50, the App should be hit 500
times. At the end of `run` it will ask the App for the number of times it
was called, to verify the count.

- - -

As noted in [the main README](../README.md), this sample has two pieces:

- a `build` script which will build the container image(s) used
- a `run` script which deploys resources that use those images

The main purpose of this example is the `run` script, but the `build`
script is included for complete educational (and reuse) purposes.
