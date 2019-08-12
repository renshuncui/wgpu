This is an active GitHub mirror of the WebGPU native implementation in Rust, which now lives in [Mozilla-central](https://hg.mozilla.org/mozilla-central). Issues and pull requests are accepted, but we merge them in m-c manually and then sync to GitHub instead of landing directly here.

---
# WebGPU
[![Build Status](https://travis-ci.org/gfx-rs/wgpu.svg)](https://travis-ci.org/gfx-rs/wgpu)
[![Crates.io](https://img.shields.io/crates/v/wgpu-native.svg?label=wgpu-native)](https://crates.io/crates/wgpu-native)
[![Gitter](https://badges.gitter.im/gfx-rs/webgpu.svg)](https://gitter.im/gfx-rs/webgpu)

This is an experimental [WebGPU](https://www.w3.org/community/gpu/) implementation as a native static library. It's written in Rust and is based on [gfx-hal](https://github.com/gfx-rs/gfx) and [Rendy](https://github.com/amethyst/rendy) libraries. The corresponding WebIDL specification can be found at [gpuweb project](https://github.com/gpuweb/gpuweb/blob/master/spec/index.bs).

The implementation consists of the following parts:
  1. `wgpu-native` - the native implementation of WebGPU as a C API library
  2. `wgpu-remote` - remoting layer to work with WebGPU across the process boundary
  3. `ffi` - the C headers generated by [cbindgen](https://github.com/eqrion/cbindgen) for both of the libraries

## Supported Platforms

   API   |       Windows      |       Linux        |    macOS & iOS     |
  -----  | ------------------ | ------------------ | ------------------ |
  DX11   | :heavy_check_mark: |                    |                    |
  DX12   | :heavy_check_mark: |                    |                    |
  Vulkan | :heavy_check_mark: | :heavy_check_mark: |                    |
  Metal  |                    |                    | :heavy_check_mark: |
  OpenGL |                    |                    |                    |

## Usage

This repository contains C-language examples that link to the native library targets and perform basic rendering and computation. Please refer to our [Getting Started](https://github.com/gfx-rs/wgpu/wiki/Getting-Started#getting-started) page at the wiki for more information.

Bindings:
  - https://github.com/gfx-rs/wgpu-rs - idiomatic Rust wrapper with [a few more examples](https://github.com/gfx-rs/wgpu-rs/tree/master/examples) to get a feel of the API
  - https://nest.pijul.com/porky11/wgpu - experimental [Scopes](http://scopes.rocks) wrapper
