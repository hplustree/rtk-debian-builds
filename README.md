# RTK Debian Builds

Custom builds of `rtk-ai` for Debian Bookworm (GLIBC 2.36).

## Purpose

This repository was created to store pre-built `rtk-ai` binaries to optimize the deployment pipeline for the `mostlyagent2` project. 

By hosting custom Debian Bookworm builds here, we decouple the heavy lifting of building `rtk-ai` from the main application. 

**Note:** This repository does not contain source code in its branches. The compiled binaries are built locally and published directly to the **[GitHub Releases](https://github.com/hplustree/rtk-debian-builds/releases)** page.

## Available Architecture Builds

Currently, releases are published with binaries for the following architectures:
- `aarch64` (ARM64)
- `x86_64` (AMD64)

### Example Usage

You can download the artifacts directly from the Releases page. Here is an example of fetching the `v0.29.0` release for `x86_64`:

```bash
wget https://github.com/hplustree/rtk-debian-builds/releases/download/v0.29.0/rtk-v0.29.0-x86_64-linux-bookworm.tar.gz
```

For ARM64 architectures (like AWS Graviton or Apple Silicon):

```bash
wget https://github.com/hplustree/rtk-debian-builds/releases/download/v0.29.0/rtk-v0.29.0-aarch64-linux-bookworm.tar.gz
```

## Integration with `mostlyagent2`

The `mostlyagent2` repository utilizes these builds to significantly speed up its CI/CD pipeline and local development setup:
- **Optimized Docker Builds:** `mostlyagent2` uses a multi-layered approach, separating system-level dependencies (which includes fetching `rtk` from this repository's releases) from the application codebase.
- **Faster Build Times:** Downloading these pre-built binaries reduces the `rtk` setup time in the deployment workflow from minutes to just seconds, avoiding repeated installations or builds from scratch.
