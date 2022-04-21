bpftrace_local_manifest
=======================

A local `repo` manifest for easy inclusion of
[`bpftrace`](https://github.com/iovisor/bpftrace) into an AOSP build.

### Usage

In your AOSP checkout, navigate to the hidden `.repo` folder and create another
folder, `local_manifests`. Then move `bpftrace_for_android.xml` into this
folder.

On `repo sync` (you may have to usage `--force-sync` if you are using an
existing checkout), the overlay repositories will be pulled in.

Lastly, depending on how you intend to consume `bpftrace`, you may need to add
it to a product in order for it to be included in the next regular build or
build it directly via `mmma external/bpftrace/bpftrace` or similar.
