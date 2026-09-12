# C03e-RY — Fallible Generic Producer Specialization Source-Seam Selection

Status: `SELECTION — VALIDATION PENDING`

Boundary:

`PRODUCTION_DURABLE_POST_AUTH_FALLIBLE_VERIFIER_TIME_REQUESTER_RENDEZVOUS_EXPECTED_DEVICE_ADMISSION_GENERIC_PRODUCER_SPECIALIZATION_SOURCE_SEAM_SELECTION`

Selected future boundary:

`PRODUCTION_DURABLE_POST_AUTH_FALLIBLE_VERIFIER_TIME_REQUESTER_RENDEZVOUS_EXPECTED_DEVICE_ADMISSION_GENERIC_PRODUCER_SPECIALIZATION_SOURCE_MATERIALIZATION`

## Exact predecessor

Evidence-closed C03e-RX:

- head `99394429f3dbe190004821c57a2552bbd7aa8a55`;
- tree `377c5ae590339cc2ac8a3b59ab42e6c529a10d9c`;
- endpoint source blob `56f565768a61803ababa26fcbe8a3fe19d32645d`;
- PR #614 remains draft/open/unmerged/mergeable and evidence-closed;
- immutable RX audit Drive ID `13Mewtwp4cSLTUfGjzLXbajq4uHC2_SbS`;
- RX audit bytes `15179`;
- RX audit SHA-256 `8a4c840907109baf137077c01b15fc2ab5ac55d69b1288949652bd9ca8a5ca8a`.

Fresh pre-RY audit re-proves the exact RX head/tree, unchanged integrated `main`, the canonical RX Drive singleton, and an empty RY branch namespace before branch creation.

## Why this seam is now feasible

Historical C03e-QO selected generic producer specialization after the older C03e-QN async producer, but C03e-QP stopped before repository mutation because the then-existing generic requester/producer stack required infallible verifier time `T: FnMut() -> u64` while QN carried a fallible verifier-time function pointer.

That historical blocker is not present in the current chain.

Fresh exact-RX source inspection proves the current C03e-RN higher endpoint-owner generic producer seam already accepts:

- `T: FnMut() -> Result<u64, prw_session::prwa_verifier_source::PrwaVerifierSourceError> + Send + 'static`;
- `H: std::ops::AsyncFnMut(DeviceId, Result<RequesterRendezvousFallibleVerifierTimeProductionDurableSchedulingWorkerStop, RemoteSessionSpawnedWorkerJoinError>) -> Receipt`;
- `Q: FnMut(DeviceId, Result<RequesterRendezvousFallibleVerifierTimeProductionDurableSchedulingWorkerStop, RemoteSessionSpawnedWorkerJoinError>) -> Receipt`;
- `O: FnMut(Receipt)`.

Therefore no verifier-time semantic translation, defaulting, retry, flattening, or lower-stack signature widening is required to specialize the generic producer seam to the already-materialized fallible receipt family.

## Existing authorities to be composed, not rewritten

The future materialization must reuse unchanged:

1. C03e-RN higher endpoint-owner fallible generic producer forwarding:
   `drive_repeated_real_remote_admission_endpoint_lifecycle_with_production_durable_fallible_verifier_time_scheduling_producer(...)`;
2. C03e-RX live async producer:
   `produce_remote_session_expected_device_admission_with_fallible_verifier_time_and_fallible_receipt(...)`;
3. C03e-RT synchronous shutdown-suppression mapper:
   `map_remote_session_expected_device_admission_fallible_verifier_time_shutdown_suppression(...)`;
4. existing fallible receipt:
   `RemoteSessionExpectedDeviceAdmissionFallibleVerifierTimeHandoffReceipt`.

The future stage must not rewrite the RR classifier, RT mapper, RV request-construction seam, RX producer, RN higher forwarding seam, lower cooperative producer driver, or receipt representation.

## Future hard source ceiling

A future separately gated C03e-RZ source checkpoint may modify exactly one Rust path:

`crates/prw-agent/src/remote_session_capability_runtime/remote_session_endpoint_lifecycle_runtime.rs`

Required predecessor blob:

`56f565768a61803ababa26fcbe8a3fe19d32645d`

If correct materialization requires a second Rust path, parent re-export, visibility widening outside this private module, lower driver mutation, dispatcher-source capture, channel construction, receiver transfer, caller migration, or runtime/network activation, the source checkpoint must STOP and return to selection.

## Selected future adapter shape

The future source stage may add only one private dormant same-file specialization adapter.

Its role is to bind the already-generic RN endpoint-owner producer seam to the existing fallible receipt family without activating production ownership outside the current module.

Conceptually, it may:

- accept the same endpoint-owner lifecycle authorities/inputs already required by RN;
- accept one caller-owned mutable dispatcher factory borrow compatible with RX;
- accept one borrowed typed production sender compatible with RX;
- accept one caller-supplied receipt observer `O: FnMut(RemoteSessionExpectedDeviceAdmissionFallibleVerifierTimeHandoffReceipt)`;
- construct exactly one local async producer closure that delegates each live producer invocation exactly once to RX;
- pass RT as the synchronous shutdown-suppression mapper;
- invoke the existing RN higher endpoint-owner generic producer forwarding exactly once;
- return RN's existing `Result<(), RemoteSessionPersistentCollectionConfigError>` unchanged.

Exact helper naming and rustfmt layout are not semantic.

## Live producer closure law

The local async producer closure must preserve exact callback inputs supplied by the generic driver:

- requester callback `DeviceId`;
- exact fallible scheduling-worker completion.

For each live invocation it must delegate exactly once to:

`produce_remote_session_expected_device_admission_with_fallible_verifier_time_and_fallible_receipt(...)`

using only the caller-supplied dispatcher-factory borrow and borrowed typed sender.

The specialization adapter must not reproduce RX classification, request construction, send, receipt composition, identifier generation, scheduling-grant handling, or verifier-time binding.

It must not add a second producer future, spawn a task, detach work, queue producer invocations, or retain a producer future outside the existing generic driver.

## Shutdown suppression law

The specialization must pass exactly:

`map_remote_session_expected_device_admission_fallible_verifier_time_shutdown_suppression(...)`

as the generic seam's synchronous suppression mapper.

Shutdown-recovered completion before producer start therefore remains:

`existing lower peer disposition -> RT suppression mapper -> receipt observer`.

An RX producer future that has already started remains owned/driven by the existing generic cooperative producer machinery and must terminate to its own one receipt. Supervisor shutdown must not retroactively replace, cancel, or remap that already-started producer result through RT.

Receiver/channel closure inside RX remains `ChannelClosed`; it is not supervisor shutdown.

## Receipt observer law

The future adapter may accept one caller-supplied receipt observer consuming:

`RemoteSessionExpectedDeviceAdmissionFallibleVerifierTimeHandoffReceipt`.

It must forward that observer unchanged into the existing generic seam.

The adapter must not:

- inspect receipt internals;
- project receipt variants;
- clone/copy/reconstruct receipts;
- persist receipts;
- convert to the historical non-fallible receipt family;
- invent higher receipt-observation policy.

Higher receipt interpretation remains separately gated.

## Pending producer-future custody law

The existing generic cooperative driver remains sole owner of pending producer-future custody and arbitration.

The future adapter must not create another pending-future owner, supervisor task, join handle, timeout, cancellation token, retry loop, or background executor.

No callback `block_on` is selected.

## Dispatcher factory law

The future adapter may only borrow a caller-supplied dispatcher factory compatible with RX.

It must not:

- capture the concrete production dispatcher source/factory from status or control-plane state;
- widen the dispatcher factory visibility;
- memoize or clone the dispatcher factory;
- pre-create a dispatcher before RX eligibility permits it;
- add retry/fallback dispatcher construction.

Concrete production dispatcher-source capture remains separately gated.

## Sender/channel law

The future adapter may only borrow the caller-supplied typed sender needed by RX.

It must not:

- construct the production channel;
- split sender/receiver ownership;
- clone the sender;
- store the sender;
- create a spare/fallback sender;
- create a second channel;
- use `try_send`, `blocking_send`, reserve/try-reserve alternate protocols, callback `block_on`, retry/requeue, timeout escape, or an unbounded queue.

RX remains sole owner of one `sender.send(request).await` per constructed handoff.

Production channel construction and exact sender/receiver ownership split remain separately gated.

## Identity and scheduling authority law

The specialization must preserve existing authority identities unchanged:

- requester callback `DeviceId` remains requester-side correlation only;
- target expected `DeviceId` remains sourced only from the scheduling grant consumed by RV;
- requester scheduling `SessionId` remains distinct from target admission `SessionId`;
- target admission `SessionId` and authentication request ID remain sourced only by RV;
- acknowledgement result remains orthogonal and exact;
- scheduling grant remains one-shot, non-`Copy`, non-`Clone`;
- no grant remint/replay/refund/rollback/reconstruction;
- no scheduling-consumption reversal.

The specialization adapter itself must never inspect or destructure the scheduling grant.

## Verifier-time law

The future adapter must preserve the existing fallible verifier-time stack unchanged.

It must not:

- sample verifier time itself;
- convert `Result<u64, PrwaVerifierSourceError>` to infallible `u64`;
- default, retry, cache, suppress, flatten, or panic on verifier-time failure;
- create a second time source.

The current fallible generic endpoint seam and lower requester stack remain authoritative.

## Endpoint-owner and lower-driver law

The future adapter must not reproduce endpoint-owner cleanup or lower cooperative-driver behavior.

C03e-RN remains sole higher endpoint-owner forwarding authority for:

- consuming the endpoint lifecycle owner exactly once;
- retaining executor/transport/supervisor-shutdown ownership ordering;
- forwarding the fallible generic producer seam;
- preserving lower close / wait-idle ownership.

The lower generic producer driver remains sole authority for producer/admission/worker quiescence and shutdown arbitration.

## Explicitly deferred beyond future source materialization

Still separately gated:

- concrete production dispatcher-source capture;
- status snapshot acquisition/refresh policy;
- production MPSC channel construction;
- exact sender/receiver ownership split;
- sole-sender higher-owner custody;
- receiver transfer into a higher expected-device admission owner;
- higher receipt observation/interpreting policy;
- requester/rendezvous higher-owner integration;
- process/runtime caller migration;
- executable caller wiring;
- endpoint/listener/bootstrap/readiness/network activation;
- database/auth/control-plane mutation;
- Cargo/lockfile mutation;
- final workflow mutation;
- Android source mutation;
- packaging/service/repository configuration;
- deployment;
- merge;
- ready-for-review conversion;
- PR closure;
- branch deletion;
- reset/rebase/squash/force/history rewrite;
- destructive evidence cleanup.

No ordering among independent later ownership/integration gates is invented here.

## Validation authority for RY

C03e-RY is documentation-only.

All PASS claims must bind only to the exact final RY head after this contract commit.

Expected path-filter behavior:

- PRW Rust Validation must run and pass;
- C02f-AD / C02f-AE may be `SKIPPED`; `SKIPPED` is not PASS;
- no Android PASS may be claimed unless an exact-head Android workflow actually runs.

No predecessor CI result may be inherited as RY validation authority.

## Stable main guard

Integrated `main` must remain unchanged at:

- head `7c993fa93977a0bb84e0d030874eee7fd0cae77f`;
- tree `63b8e59ca53797fdea6b95432e16f35eaf473604`.

## Transparent connector no-op record

Before real RY branch creation, two placeholder PR create probes using invalid `__never__` base/head refs were rejected by GitHub with HTTP 422 Validation Failed.

They created no PR, branch, ref, file or commit and changed no repository or Drive evidence state.

## Closure protocol

After exact-head validation:

1. freeze immutable RY audit bytes at `SELECTION — VALIDATED — EVIDENCE PUBLICATION PENDING`;
2. perform exact-title zero-collision search in canonical Drive parent immediately before upload;
3. upload exactly once;
4. verify metadata, byte count, raw bytes, SHA-256, final LF, singleton exact-title result and one initial revision;
5. update the RY PR body to `SELECTION — VALIDATED — EVIDENCE_RECORDED — CLOSED`;
6. re-read RY head/tree/contract blob, PR, `main`, Drive singleton/revision and successor namespace;
7. STOP.

Do not materialize the selected source inside C03e-RY.
