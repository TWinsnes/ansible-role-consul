# 2. extract consul role

Date: 2018-07-30

## Status

Accepted

## Context

Consul is being installed as a part of a vault deployment, should we extract the consul role for re-usability?

## Decision

Extract the consul role, as there are more benefits in reusability of the role, rather than having it set up specifically for our use case

## Consequences

The role will have to be managed externally to the deployment of Vault and it has to be more generic. A bit more work will be required to make sure it is generic and documented in its own right.
