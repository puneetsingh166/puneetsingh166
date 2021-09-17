* when we are running this command 
 ``` 
 aurora install --chain 1313161556 --owner test.near mainnet-release.wasm 
 
 ```
 error is coming on aurora CLI -

 ```
 hread 'main' panicked at 'AVX support is required in order to run Wasmer VM Singlepass backend.', runtime/near-vm-runner/src/wasmer_runner.rs:232:9
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
Sep 17 16:55:47.541 WARN jsonrpc: Timeout: tx_polling method. tx_info Transaction(SignedTransaction { transaction: Transaction { signer_id: AccountId("aurora.test.near"), public_key: ed25519:6LtQN9JyJGATDYHGMUJm1rA15phQ8PvuRp8CqZb7V2NC, nonce: 17581000002, receiver_id: AccountId("aurora.test.near"), block_hash: `3EvuMvrTDpUQfQjMq3LMBeWYgKdissYbw269AGmp4Y5N`, actions: [FunctionCall(FunctionCallAction { method_name: new, args: `NEAT test.near`, gas: 300000000000000, deposit: 0 })] }, signature: ed25519:qutftEiXY2g92F9MyFg5GKxhwMa4qdpoHc6rGJa9btgwCngkGZbraTEHoSp8d3nms6dSXLPBLKpK1yUdkiLKw1J, hash: `8q1S3AhajNVFmrNYJD9AKYbNhEzeUTnB1P1ie2oTq865`, size: 210 })
```

or 

* when we are running this command
```
aurora --signer aurora.test.near --engine aurora.test.near  install --chain 1313161556 --owner test.near betanet-release.wasm

```
error is coming on aurora CLI -
```
[5:52 PM] Puneet Singh
bigint: Failed to load bindings, pure JS will be used (try npm run rebuild?)
Retrying request to broadcast_tx_commit as it has timed out [
'CQAAAHRlc3QubmVhcgBeJjdaDRj//l/YqBI07Oax4xz3jpB9IcDRWZiTiGf/FwQAAAAAAAAAEAAAAGF1cm9yYS50ZXN0Lm5lYXLpl0rH+GXXAEzcq2YQa0QTacUhWzguRtc86MfZol7A6QEAAAACAwAAAG5ldzkAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAATkVBVAkAAAB0ZXN0Lm5lYXIAAAAAAAAAAAAAAAAAwG4x2RABAAAAAAAAAAAAAAAAAAAAAAAAPlMzCu8J3aB7g/wC4lJj/44VL7Sca9j9ptBkeb/cvVTD6ifPS5ae2er36AsiDTJVlUcOgO8MF+WPWkgTjD7TDQ=='
]
TypedError: [-32000] Server error: The node reached its limits. Try again later. More details: Mailbox has closed
at /usr/lib/node_modules/@aurora-is-near/cli/node_modules/near-api-js/lib/providers/json-rpc-provider.js:179:31
at processTicksAndRejections (internal/process/task_queues.js:95:5)
at async Object.exponentialBackoff [as default] (/usr/lib/node_modules/@aurora-is-near/cli/node_modules/near-api-js/lib/utils/exponential-backoff.js:7:24)
at async JsonRpcProvider.sendJsonRpc (/usr/lib/node_modules/@aurora-is-near/cli/node_modules/near-api-js/lib/providers/json-rpc-provider.js:154:24)
at async /usr/lib/node_modules/@aurora-is-near/cli/node_modules/near-api-js/lib/account.js:94:24
at async Object.exponentialBackoff [as default] (/usr/lib/node_modules/@aurora-is-near/cli/node_modules/near-api-js/lib/utils/exponential-backoff.js:7:24)
at async Account.signAndSendTransaction (/usr/lib/node_modules/@aurora-is-near/cli/node_modules/near-api-js/lib/account.js:90:24)
at async Engine.callMutativeFunction (file:///usr/lib/node_modules/@aurora-is-near/cli/node_modules/@aurora-is-near/engine/lib/engine.js:312:28)
at async Engine.promiseAndThen (file:///usr/lib/node_modules/@aurora-is-near/cli/node_modules/@aurora-is-near/engine/lib/engine.js:85:19)
at async Engine.initialize (file:///usr/lib/node_modules/@aurora-is-near/cli/node_modules/@aurora-is-near/engine/lib/engine.js:80:20) {
type: 'UntypedError',
context: ErrorContext {
transactionHash: 'W6yESvHmQ4LtoAVXSvHmHWgQw3na7ArCuqoeY4xqnS1'
}
}
(node:5706) UnhandledPromiseRejectionWarning: ReferenceError: Cannot unwrap Ok value of Result.Err
at Object.unwrap (/usr/lib/node_modules/@aurora-is-near/cli/node_modules/@hqoss/monads/dist/lib/result/result.js:70:19)
at Command.<anonymous> (file:///usr/lib/node_modules/@aurora-is-near/cli/lib/aurora.js:30:66)
at processTicksAndRejections (internal/process/task_queues.js:95:5)
(Use `node --trace-warnings ...` to show where the warning was created)
(node:5706) UnhandledPromiseRejectionWarning: Unhandled promise rejection. This error originated either by throwing inside of an async function without a catch block, or by rejecting a promise which was not handled with .catch(). To terminate the node process on unhandled promise rejection, use the CLI flag `--unhandled-rejections=strict` (see https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode). (rejection id: 1)
(node:5706) [DEP0018] DeprecationWarning: Unhandled promise rejections are deprecated. In the future, promise rejections that are not handled will terminate the Node.js process with a non-zero exit code.
Command-line options | Node.js v16.9.1 Documentation

```

along these above two errors the warning coming on near validator node side -

```
       stats: Server listening at ed25519:4fshaPnurZkJbeL3wtHWYwtx2qid2obp1Nsf57yoTWKC@0.0.0.0:24567
thread 'main' panicked at 'AVX support is required in order to run Wasmer VM Singlepass backend.', runtime/near-vm-runner/src/wasmer_runner.rs:232:9
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
thread '<unnamed>' panicked at 'AVX support is required in order to run Wasmer VM Singlepass backend.', runtime/near-vm-runner/src/wasmer_runner.rs:232:9
  ```

 
