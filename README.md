# PicoFake8

PicoFake8 is being converted to use the **actual FAKE-08 emulator source** from jtothebell/fake-08.

## Current state

The repository still contains the earlier lightweight compatibility player. It is **not** being described as FAKE-08.

A GitHub Actions build has now been added that:

1. checks out the upstream FAKE-08 repository with its submodules;
2. builds its libretro source with Emscripten;
3. links those upstream objects into a browser WebAssembly module;
4. copies the upstream FAKE-08 license into the build output;
5. uploads the generated browser core as a GitHub Actions artifact.

The browser frontend is deliberately not claimed to be finished yet. The existing player remains in place until the upstream core build and a compatible browser frontend are actually verified.

## Runtime requirements

The eventual published page is intended to contain the generated JavaScript/WASM locally, with no CDN, iframe, or runtime external dependency.

## Upstream

FAKE-08:
https://github.com/jtothebell/fake-08

FAKE-08 is not PICO-8 and is not related to or supported by Lexaloffle Software.
