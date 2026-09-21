# Vendored third-party code

Files under assets/js that are not initMAX code, with the exact upstream, licence and what changed. `tests/injection.php` verifies the checksums.

| file | upstream | licence | changed |
|---|---|---|---|
| chess.js | chess.js 0.13.4, npm `chess.js@0.13.4` (Jeff Hlywa) | BSD-2-Clause | wrapped in an IIFE exposing only `window.Chess`; the ES `export` keywords removed - nothing else |
| stockfish-17.1-lite-single-03e3232.js + .wasm | Stockfish.js 17.1, npm `stockfish@17.1.0` src/ (nmrugg/stockfish.js, (c) Chess.com), single-threaded lite NNUE build | GPLv3 | unmodified |

## Checksums (sha256)

```
399d3e6437dac6d91217f9909de47b23ac6046bbb9f8c64baf4079003673e8c4  chess.js
1c8265e52fdaef797684b4979b42c5dcfe0350df3e11a87e48e4ec5f86e0ca5c  stockfish-17.1-lite-single-03e3232.js
7ca31bedd166148931a1cc84dbd8dd9cf001744e9994caf23a3c6ff4988d7086  stockfish-17.1-lite-single-03e3232.wasm
```
