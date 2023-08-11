# Test JOb

This sample shows up to run a batch job. This is very similar to the
[job](../job) sample but this code will allow you to modify the behavior
of the code through the following environment variables:
  - `MSG` : specifies the message printed to the logs. By default it will be
    a simple "Hello World" type of message
  - `TARGET` : When the default message is printed, you can change the word
    "World" to something else by setting the `TARGET` environment variable.
  - `SLEEP` : will tell the code to sleep for the specified number of seconds
    before exiting.
  - `CRASH` : will tell the code to exit with a non-zero exit code. This is
    useful if you want to test the job "retry" logic.

The code will also print the list of environment variables to the log file
for debugging purposes.

The sample script will also submit the job twice. First by creating a
job definition, followed by submitting it, and then it will submit a new
job directly without first creating a job definition. In the second case
it will also change the message printed via the `MSG` environment variable.

- - -

As noted in [the main README](../README.md), this sample has two pieces:

- a `build` script which will build the container image(s) used
- a `run` script which deploys resources that use those images

The main purpose of this example is the `run` script, but the `build`
script is included for complete educational (and reuse) purposes.
