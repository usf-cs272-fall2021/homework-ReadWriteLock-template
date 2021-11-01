ReadWriteLock
=================================================

![Points](../../blob/badges/points.svg)

For this homework assignment, you will create a conditional read write lock and a thread safe indexed set using that lock.

## Hints ##

Below are some hints that may help with this homework assignment:

  - Look at the lecture notes for discussion on the simple custom read write lock and how it can be used.

  - The lecture notes discuss a simple read write lock, but the one you must create is more complicated. In addition to tracking the number of readers and writers, it must track the **active** writer as well.

      This includes *setting the active writer* when a thread acquires the write lock and *unsetting the active writer* when the lock is *fully* released. The active writer can acquire additional read or write locks as long as it is the active writer.

      **Leave this part for the end, after you have a simple read write lock already working.**

  - The Javadoc is written to give clues on what conditions the code should call the `wait()` or `notifyAll()` methods.

  - When using the custom lock, decide whether a block of operations are read operations, write operations, or mixed read and write operations with respect to the **shared** data.

  - Passing the provided tests consistently is a good sign, but the tests may not catch all implementation issues. However, any time a test fails indicates there is a multithreading problem somewhere (even if it sometimes passes). Logging can help debug these cases.

These hints are *optional*. There may be multiple approaches to solving this homework.


## Requirements ##

See the Javadoc and `TODO` comments in the template code in the `src/main/java` directory for additional details. You must pass the tests provided in the `src/test/java` directory. Do not modify any of the files in the `src/test` directory.

See the [Homework Guides](https://usf-cs272-fall2021.github.io/guides/homework/) for additional details on homework requirements and submission.
