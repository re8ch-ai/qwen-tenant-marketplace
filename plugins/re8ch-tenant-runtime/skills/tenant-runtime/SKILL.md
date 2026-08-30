---
name: tenant-runtime
description: Plan and operate Qwen-scoped OCI container runs and database instances on RE8CH capacity.
---

# Tenant Runtime

Use only `re8ch-qwen-runtime`. Discover capacity and plan before every write.
The authenticated identity fixes tenant `qwen`; never accept a tenant override.
Run only immutable OCI digests. Ordinary containers may be executed through
containerd/Kubernetes and do not require serverless or Nuclio. Database runs
must declare engine, image digest, storage, backup, retention, resource quota,
and expiry. Return opaque runtime, database, log, artifact, and connection
references only. Never return credentials or invoke raw kubectl, SSH,
containerd, Ceph, Cilium, or database administrator operations. Stop or release
only references owned by the authenticated tenant.
