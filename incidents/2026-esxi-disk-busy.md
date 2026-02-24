# Incident: ER)©¢ª[j«∫·Õ—°…Ω’ù†Å5Ö…≠ïêÅÖÃÅ	’Õ‰((¥Ä®®Date:** 2026
- **everity:** Medium
- **Component:** VMware ESXi (N6005 Host)
- **Status:** Resolved

## Summary
While attempting to modify disk passthrough configuration on my N6005 ESXi host, the target disk was reported as "busy" by the VMkernel.

## Root Cause
The disk was still referenced by the hypervisor due to internal storage bindings/locks.

## Resolution
- Verified no active VM was using the disk
- Checked datastore/device mappings
- Rebooted host to clear lingering locks
- Re-applied configuration successfully
