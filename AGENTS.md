# Accepted Software Delivery Receiver Service

This SDSS-owned service separates customer acceptance, receiver-local
staging, and SDSS-local admission. It exposes two separately offered and
invoked create-only operations, plus a separately offered and invoked
correction staging/admission pair. Correction binds the complete intended
source plate through the accepted product. `data` and `node_modules` are exact
preserved runtime roots: they are neither traversed nor replaced. It binds
their path/inode snapshots and the replaceable plate digest before staging and
immediately before/after publication. It prepares private replacement-plate
and displaced-plate directories, records a crash-recoverable per-entry rename
state, commits the new plate, and removes displaced live plate bytes.
It never provides a live fallback branch. No operation accepts ambient paths,
discovers a roster, writes across a settlement, or grants authority to install
this service itself. Its signed A2A face is the only cross-settlement carrier;
the receiver acts only within its fixed SDSS authority root.

All runtime evidence is content-addressed and append-only. A staging capability
and an admission grant are distinct, human-issued, expiring, at-most-once
authorities. Admission imports the adopted mesh-scope carrier and binds its
request SHA-256 and filesystem snapshot; it does not restate the classifier.
