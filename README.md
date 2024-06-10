# Instructions

- Run `npm install` to install the dependencies.
- Run `npm run test` to run the tests in watch mode.
- Add code to the relevant source code files in the `src` directory and save to re-run the tests.
- **You DO NOT need to optimize your code! Just get the tests to pass and you're good!**
- _**Console logs will be printed at the beginning of the test output in the terminal below.**_

# Challenge spec

Given an async function and a limit where:
- `fn` - async function
- `limit` - non-negative number

Implement the function `asyncRetry` (in [`asyncRetry.ts`](src/asyncRetry.ts)) that will retry the async function `fn` up to `limit` number of times. If `fn` fails, it should retry again immediately. `asyncRetry` should return the result of `fn` once it succeeds. If `fn` fails `limit` times, it should throw the error thrown by `fn`.
