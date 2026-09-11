# D4DR4T

> **Status: archived defensive design concept.** This repository contains documentation only. It has no executable agent, controller, release, or supported deployment.

D4DR4T is retained as a record of a possible consent-based endpoint security lab. It is not a remote-access product and is not intended for use on production systems.

## Safety reset

An earlier description proposed capabilities that are incompatible with this project's safe scope. Those proposals are superseded and explicitly repudiated. This project will not collect credentials, passwords, browser cookies, authentication tokens, or messaging, gaming, or browser sessions. It will not implement persistence, autorun, stealth, evasion, virtual-machine avoidance, security-control bypasses, or installation of AnyDesk or any other secondary remote-access tool.

Destructive and disruptive controls are also prohibited, including boot loops, operating-system "kill" techniques, file destruction, forced power actions, denial of service, arbitrary remote code execution, covert surveillance, and harassment. A disclaimer does not make those capabilities safe, and contributions that add them will not be accepted.

## Allowed scope

Any future experiment derived from this concept must be limited to:

- isolated lab systems owned by the operator, or systems covered by specific written authorization;
- synthetic identities, mock credentials, and non-sensitive test data;
- transparent, opt-in endpoint diagnostics and read-only inventory;
- defensive detection engineering and validation of monitoring controls;
- local simulations that cannot reach third-party systems or production networks; and
- a visible consent indicator plus an immediate, reliable way for a participant to stop the experiment.

Authorization must identify the systems, people, actions, data, and dates in scope. Consent must be informed, recorded, revocable, and renewed when the scope changes. Testing stops immediately when authorization expires or is withdrawn.

## Threat model and required controls

The design assumes that an operator account can be compromised, an endpoint can be misidentified, a command can exceed its intended scope, logs can be altered, and collected diagnostics can leak. A safe prototype therefore needs all of the following before it is exercised:

- explicit endpoint and command allowlists, with deny-by-default behavior;
- least-privilege execution and read-only behavior by default;
- mutually authenticated endpoints and short-lived, narrowly scoped credentials;
- no background persistence and no unattended installation path;
- network isolation and an emergency stop that fails closed;
- strict data minimization, short retention, and documented deletion procedures; and
- independent review of the authorization record and safety controls.

## Audit logs

Every attempted action should produce an append-only audit event containing a UTC timestamp, operator identity, authorized test identifier, endpoint identifier, requested action, decision, result, and reason. Logs must exclude secrets and unnecessary personal data. Access to logs should be restricted, integrity-protected, retention-limited, and reviewed after each exercise. Failed and denied actions are logged as carefully as successful ones.

## Responsible disclosure

See [SECURITY.md](SECURITY.md) for the safe reporting process. Never place live credentials, tokens, personal data, or exploit details in a public issue.

## Contributions

This is an archived concept, so feature development is closed. Documentation changes that clarify defensive boundaries, consent, auditing, or disclosure practices may be considered. Do not submit offensive code, operational payloads, persistence techniques, evasion guidance, destructive controls, or real data captured from another person.
