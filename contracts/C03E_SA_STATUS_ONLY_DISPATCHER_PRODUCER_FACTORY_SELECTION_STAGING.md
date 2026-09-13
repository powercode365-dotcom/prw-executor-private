# C03e-SA — Status-Only Dispatcher Source Capture / Producer Factory Selection

Status: `SELECTION — VALIDATION PENDING`

Boundary:

`PRODUCTION_DURABLE_POST_AUTH_FALLIBLE_VERIFIER_TIME_REQUESTER_RENDEZVOUS_EXPECTED_DEVICE_ADMISSION_STATUS_ONLY_DISPATCHER_SOURCE_CAPTURE_PRODUCER_FACTORY_SELECTION`

Selected future boundary:

`PRODUCTION_DURABLE_POST_AUTH_FALLIBLE_VERIFIER_TIME_REQUESTER_RENDEZVOUS_EXPECTED_DEVICE_ADMISSION_STATUS_ONLY_DISPATCHER_SOURCE_CAPTURE_PRODUCER_FACTORY_SOURCE_MATERIALIZATION`

## 1. Exact predecessor authority

This selection branches only from evidence-closed C03e-RZ.

Exact C03e-RZ authority:

- branch: `phase-152-c03e-rz-production-durable-post-auth-fallible-verifier-time-requester-rendezvous-expected-device-admission-generic-producer-specialization-source-materialization`
- head: `aca2abcb9d9bcada55fdc36b8743b38ae6b2498b`
- tree: `485a2f9dda4114e8b6fe88e0fcdcc4bb66e145d1`
- endpoint source blob: `eac44ccdf999a1270b056eb88330ee50b6ff97af`
- Linux bootstrap source blob: `f39c3f99b2967a0b75f1ade871f1d73a4e5d18b5`
- higher-owner source blob: `093cff1e4643f995f0cdc5e337ecfc3bbc2ec582`
- PR: `#616`, draft/open/unmerged and evidence-closed
- immutable RZ audit Drive ID: `1IUHd2F1Q_52M6WbbNoK2tUDHF7EComc5`

Integrated `main` remains outside this staged lineage and must remain unchanged at:

- head: `7c993fa93977a0bb84e0d030874eee7fd0cae77f`
- tree: `63b8e59ca53797fdea6b95432e16f35eaf473604`

## 2. Fresh exact-source finding

Exact RZ source proves the generic producer specialization is now materially available and no longer blocked by the historical C03e-QP infallible verifier-time mismatch.

The exact RZ endpoint helper remains private and dormant. It already accepts:

- a borrowed caller-owned `dispatcher_factory: &mut DF` where `DF: FnMut() -> D`;
- a borrowed typed `mpsc::Sender<RemoteSessionExpectedDeviceAdmissionRequest<D, RemoteSessionExpectedDeviceAdmissionFallibleVerifierTimeSource>>`;
- one caller-supplied receipt observer;
- the existing endpoint inputs.

It creates one local async producer closure, delegates each live invocation to the existing fallible producer helper, passes the existing shutdown-suppression mapper, and invokes the existing higher endpoint-owner fallible scheduling-producer seam.

Separately, exact RZ `linux_bootstrap.rs` already contains the dormant C03e-QJ private custody:

`LinuxAgentProductionRemoteCapabilityDispatcherSource`

That custody owns exactly one existing `LocalAgentStatusSnapshot` copied from `LocalLinuxProductionRuntimeInputs::status_snapshot()` and exposes only:

- `from_runtime_inputs(...)`, which captures the already-owned production snapshot;
- `new_dispatcher(&self)`, which creates a fresh existing `LinuxAgentProductionRemoteCapabilityDispatcher` from that exact retained snapshot.

No live status refresh, host query, readiness inference, shared mutable dispatcher state, or alternate dispatcher provenance is present.

Exact RZ higher-owner source also already contains the dormant C03e-QL capacity-one channel custody, but it remains separately gated from this selection.

## 3. Selected immediate next seam

The smallest independently materializable dependency after RZ is one private producer-owned dispatcher-factory capture in:

`crates/prw-agent/src/linux_bootstrap.rs`

Future hard source ceiling is exactly that one Rust path.

Required predecessor blob:

`f39c3f99b2967a0b75f1ade871f1d73a4e5d18b5`

A future separately gated C03e-SB source checkpoint may add only one private dormant factory-construction helper or equivalent private carrier that:

1. receives the existing `LocalLinuxProductionRuntimeInputs<'_>` only as the source of the already-owned status snapshot;
2. invokes `LinuxAgentProductionRemoteCapabilityDispatcherSource::from_runtime_inputs(...)` exactly once;
3. captures the resulting exact dispatcher source by value in one producer-owned factory closure or equivalent non-shared private custody;
4. exposes behavior equivalent to `FnMut() -> LinuxAgentProductionRemoteCapabilityDispatcher`;
5. on each factory invocation calls the existing `source.new_dispatcher()` exactly once;
6. returns only the fresh existing status-only dispatcher;
7. performs no status refresh, second snapshot construction, host/runtime state query, readiness inference, cache invalidation, watch subscription, synchronization primitive, retry, fallback, or alternate dispatcher construction.

The future seam must retain the exact QI/QJ provenance law: every dispatcher produced by the factory is derived only from the one already-owned immutable production status snapshot captured into the source.

Using the same retained snapshot to create multiple fresh dispatcher values does not authorize mutable shared dispatcher state or snapshot refresh.

## 4. Preserved separation

C03e-SA does not select or materialize:

- invocation of the RZ generic producer specialization;
- any visibility widening of the private RZ endpoint helper;
- C03e-QL channel construction or `into_parts()` ownership split;
- sender ownership transfer or sender clone;
- receiver transfer into the existing production consumer path;
- `sender.send(request).await` or any additional send path;
- receipt observation or higher receipt interpretation policy;
- requester/rendezvous higher-owner integration;
- process/runtime caller migration;
- executable/listener/readiness/network activation;
- target dialing or production reachability activation;
- database/schema/control-plane mutation;
- authentication cutover;
- Cargo/lockfile/workflow/Android-source mutation;
- packaging/service/repository configuration;
- merge, ready-for-review conversion, PR closure, branch deletion, reset, rebase, squash, force update, history rewrite, deployment or restart.

No `Arc`, `Mutex`, `RwLock`, atomic, watch channel, callback `block_on`, `try_send`, `blocking_send`, timeout escape, hidden/detached task, retry/requeue, alternate/unbounded queue/channel, second producer future, sender clone, scheduling-grant remint/replay/refund/rollback/reconstruction, verifier-time default/retry/cache/flattening, or cross-family receipt translation is selected.

## 5. Authority and identity law

The retained status snapshot and produced dispatcher are capability-dispatch implementation inputs only. They are not:

- requester identity;
- target expected-device identity;
- scheduling authority;
- authentication authority;
- admission authority;
- capability grant authority;
- endpoint authority;
- reachability proof;
- readiness proof;
- persistence key.

Requester callback `DeviceId`, target expected `DeviceId`, requester scheduling `SessionId`, target admission `SessionId`, expected-device authentication request ID, scheduling grant, verifier time, transport identity and durable capability authority remain distinct lanes.

## 6. Channel and producer law retained

The existing C03e-QL channel custody remains separately gated and unchanged:

- exactly one bounded Tokio MPSC channel;
- capacity exactly `1`;
- exactly one retained sender and one receiver;
- no sender clone;
- full channel means ordinary asynchronous backpressure;
- eventual enqueue remains `sender.send(request).await` only.

C03e-SA does not construct that channel or split its custody.

The existing RZ producer specialization remains the sole selected generic-specialization adapter. C03e-SA does not duplicate, replace, invoke or widen it.

## 7. Future SB stop conditions

Future source materialization must STOP and return to selection if correct implementation requires any of the following:

- a second Rust path;
- `pub(crate)` or broader visibility widening solely to connect this seam;
- mutation of `RemoteSessionEndpointLifecycleRuntime` source;
- mutation of higher-owner channel custody;
- new channel/sender/receiver ownership;
- live producer invocation;
- request construction/send;
- status refresh or a second status snapshot source;
- synchronization/shared mutable dispatcher state;
- runtime/executable caller activation;
- Cargo/lockfile/workflow/Android-source changes.

## 8. Validation and evidence protocol

All PASS claims for C03e-SA must bind only to its exact final documentation head. `SKIPPED` is not PASS. No RZ validation is inherited as SA validation authority.

C03e-SA is selection-only. After exact-final-head Rust validation and immutable Drive evidence publication/readback, closure truth may be recorded in the SA PR body without rewriting the frozen audit artifact.

## 9. STOP boundary

C03e-SA must remain documentation-only and draft/open/unmerged.

Do not create or materialize C03e-SB inside the C03e-SA closure. A fresh exact-head audit is required before any later source materialization.
