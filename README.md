# Instructions

- Run `npm install` to install the dependencies.
- Run `npm run test` to run the tests in watch mode.
- Add code to the relevant source code files in the `src` directory and save to re-run the tests.
- **You DO NOT need to optimize your code! Just get the tests to pass and you're good!**
- _**Console logs will be printed at the beginning of the test output in the terminal below.**_

# Challenge spec

Given an async function `fn` and a `maxRetryCount` where:
- `fn` - async function
- `maxRetryCount` - non-negative number

Implement the function `asyncRetry` (in [`asyncRetry.ts`](src/asyncRetry.ts)) that will try to invoke the async function `fn` up to `maxRetryCount` number of times. `asyncRetry` should return the result of `fn` once it succeeds. If `fn` fails (an error is thrown), it should retry again immediately. If `fn` fails `maxRetryCount` times, it should throw the error thrown by `fn`.

As an example, the async function could be a data fetching function. If the request fails, we want to try again in case of a server or network hiccup but if it fails more than `maxRetryCount` number of times, we want to throw the error, since we don't want to retry forever.
