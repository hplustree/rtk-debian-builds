# RTK Debian Builds

Custom builds of `rtk-ai` for Debian Bookworm (GLIBC 2.36).

## Purpose

This repository was created to store pre-built `rtk-ai` binaries to optimize the deployment pipeline. 

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

