<p align="center">
  <img src="img/spectre-avatar.svg" alt="Spectre ghost" width="128" height="128">
</p>

<h1 align="center">Spectre for Rabbit R1</h1>

<p align="center">An independent Linux operating system and reverse-engineering project for Rabbit R1.</p>

<p align="center">
  <a href="https://github.com/spectre-oss/rabbit-r1-kernel">Kernel</a> ·
  <a href="https://github.com/spectre-oss/rabbit-r1-os">Operating system</a> ·
  <a href="https://github.com/spectre-oss/spectre-launcher">Launcher</a>
</p>

## About

Spectre explores the Rabbit R1 hardware and builds an open Linux software stack around it: device support, an operating system, and a native launcher. The project brings together hardware reverse engineering, driver development, and a device-focused user experience.

Rabbit R1 is the first device project under [Spectre OSS](https://github.com/spectre-oss), an organization for open-source reverse-engineering work.

## Project status

**Early development · Partial kernel sources and optional compatibility patches published**

This repository is the project landing page. The [kernel repository](https://github.com/spectre-oss/rabbit-r1-kernel) now contains a reviewed partial source release and optional panel/Wi-Fi compatibility patches. The operating-system and launcher repositories remain placeholders. There is no public installable OS release yet.

The kernel release includes source provenance, build instructions, a hardware support matrix, and scoped validation records. It is not a complete, self-contained device image or a flashable release. A working development device does not imply that every feature is ready for general use.

## Repositories

| Repository | Purpose |
| --- | --- |
| [rabbit-r1](https://github.com/spectre-oss/rabbit-r1) | Project overview, documentation, and future integration repository. |
| [rabbit-r1-kernel](https://github.com/spectre-oss/rabbit-r1-kernel) | Published partial kernel sources, device support, and optional panel/Wi-Fi compatibility patches. |
| [rabbit-r1-os](https://github.com/spectre-oss/rabbit-r1-os) | Planned Spectre OS integration, image tooling, and device services; source publication pending. |
| [spectre-launcher](https://github.com/spectre-oss/spectre-launcher) | Planned native launcher and device user interface; source publication pending. |

The device components are planned to come together in this repository. The kernel component is now published separately; OS and launcher publication is still pending.

## Kernel sources, patches, and GPU dependencies

Start with the [kernel README](https://github.com/spectre-oss/rabbit-r1-kernel#readme) and [partial-release scope](https://github.com/spectre-oss/rabbit-r1-kernel/blob/main/Documentation/rabbit-r1/partial-release.md).

- **Panel and Wi-Fi:** [optional compatibility patches and preparation instructions](https://github.com/spectre-oss/rabbit-r1-kernel/tree/main/patches/rabbit-r1) explain how to combine our changes with separately downloaded, pinned Rabbit sources. The original panel command table, complete vendor Wi-Fi sources, and four deferred Wi-Fi inputs are not bundled in the patch set.
- **Rabbit's public originals:** [kernel sources](https://github.com/rabbit-hmi-oss/android_kernel_rabbit_mt6765) and [module sources](https://github.com/rabbit-hmi-oss/android_kernel_modules_rabbit_mt6765). The [source guide](https://github.com/spectre-oss/rabbit-r1-kernel/blob/main/Documentation/rabbit-r1/external-sources-and-gpu-blobs.md) gives exact commits and file paths.
- **GPU blobs:** obtain the reference stock image from Rabbit's official [rabbitOS v0.8.293 release](https://github.com/rabbit-hmi-oss/firmware/releases/tag/v0.8.293). The same [source and GPU guide](https://github.com/spectre-oss/rabbit-r1-kernel/blob/main/Documentation/rabbit-r1/external-sources-and-gpu-blobs.md) identifies firmware and userspace libraries and describes offline extraction. Proprietary blobs are not hosted here.
- **Validation and limits:** the patches applied cleanly, the panel module compiled, and all four Wi-Fi/connectivity modules matched the prior verified build byte-for-byte. See the [patch validation record](https://github.com/spectre-oss/rabbit-r1-kernel/blob/main/patches/rabbit-r1/validation.json) and [hardware scope](https://github.com/spectre-oss/rabbit-r1-kernel/blob/main/Documentation/rabbit-r1/hardware.md). These checks are not a new device test or a claim of general installation readiness.

## Remaining release priorities

- Publish the remaining OS and launcher sources with provenance and retained license notices.
- Extend the documented build and validation process to the remaining components.
- Maintain the kernel hardware support matrix and distinguish verified behavior from experimental features.
- Document firmware dependencies, installation prerequisites, known issues, and recovery procedures before distributing bootable images.

## Contributing

During release preparation, use [project issues](https://github.com/spectre-oss/rabbit-r1/issues) for focused questions, hardware findings, and documentation suggestions. Include the relevant hardware revision, software version, and reproducible evidence where available. Remove credentials and personal or device-specific identifiers from logs before sharing them.

Kernel build and optional-patch instructions are available in the links above. OS and launcher build instructions will accompany their source releases.

## Attribution and licensing

Spectre builds on the work of the Linux community and device bring-up contributors. The published kernel source retains upstream and vendor notices and documents code provenance. Original Spectre kernel contributions use GPL-2.0-only; see the [kernel licensing policy](https://github.com/spectre-oss/rabbit-r1-kernel/blob/main/Documentation/rabbit-r1/licensing-policy.md). Panel/Wi-Fi input licensing questions remain deferred; optional patches do not declare those questions resolved. This landing page does not assign a blanket license to future components or third-party artwork.

Spectre OSS is an independent community project and is not affiliated with or endorsed by Rabbit Inc. Product names and trademarks belong to their respective owners.
