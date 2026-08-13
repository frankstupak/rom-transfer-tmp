# rom-transfer-tmp

A private, deliberately ephemeral file bridge. It exists to hand a build artifact between an
isolated environment and the Lumen homelab fleet when no direct network path is available:
push on one side, pull on the other, empty it afterwards.

**Status: transient by design.** The repository is expected to be empty most of the time. Nothing
here is a library, nothing has a stable path, and no contents should be treated as durable — a
transfer that has completed gets cleared. It is not intended for outside use.

Most fleet transfers use `scp` over Tailscale or the standing restic repositories instead; this
bridge is only for the cases where neither endpoint can reach the other.
