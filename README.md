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

**Early development · Public source release in preparation**

This repository is currently the project landing page. Development code is being prepared for publication; the component repositories are placeholders until their initial source imports. There is no public installable OS release yet.

Existing development results will be documented alongside the corresponding source, build instructions, and known limitations. A working development device does not imply that every feature is ready for general use.

## Repositories

| Repository | Purpose |
| --- | --- |
| [rabbit-r1](https://github.com/spectre-oss/rabbit-r1) | Project overview, documentation, and future integration repository. |
| [rabbit-r1-kernel](https://github.com/spectre-oss/rabbit-r1-kernel) | Linux kernel changes and device support for Rabbit R1. |
| [rabbit-r1-os](https://github.com/spectre-oss/rabbit-r1-os) | Spectre OS system integration, image tooling, and device services. |
| [spectre-launcher](https://github.com/spectre-oss/spectre-launcher) | Native launcher and device user interface. |

The device components are planned to come together in this repository. Component repositories remain the intended publication destinations during initial preparation.

## Initial release priorities

- Publish reviewed source with upstream provenance and retained license notices.
- Document the build environment and verify builds from clean checkouts.
- Publish a hardware support matrix that distinguishes verified behavior from experimental features.
- Document firmware dependencies, installation prerequisites, known issues, and recovery procedures before distributing bootable images.

## Contributing

During release preparation, use [project issues](https://github.com/spectre-oss/rabbit-r1/issues) for focused questions, hardware findings, and documentation suggestions. Include the relevant hardware revision, software version, and reproducible evidence where available. Remove credentials and personal or device-specific identifiers from logs before sharing them.

Build and contribution instructions will accompany the source releases.

## Attribution and licensing

Spectre builds on the work of the Linux community and device bring-up contributors. Source releases will retain their original copyright and license notices and document imported code and its provenance. This landing page does not assign a blanket license to future components or third-party artwork.

Spectre OSS is an independent community project and is not affiliated with or endorsed by Rabbit Inc. Product names and trademarks belong to their respective owners.
