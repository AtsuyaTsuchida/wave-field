# WAVE FIELD — Quantum / Classical Wave Simulator

[English](#english) | [日本語](#日本語)

---

## English

A dual-engine wave-field simulator that runs entirely in a single WebGL2 HTML file.
It switches between a **quantum** engine (the time-dependent Schrödinger equation, integrated with the Visscher real/imaginary leap-frog scheme) and a **classical** engine (the scalar wave equation), so you can compare how probability amplitude and a classical field propagate through the same geometry.

### Run
```sh
cd ~/dev/wave-field
python3 -m http.server 8180
# → http://localhost:8180/
```

### Features
- **Quantum engine** — Schrödinger evolution via Visscher's staggered real/imaginary update (stable, norm-preserving).
- **Classical engine** — second-order scalar wave equation on the same grid.
- **Presets** — double slit, single slit, barrier/tunnelling, free wave packet, and more.
- **Sources** — inject Gaussian wave packets, or drive the field from the **microphone**.
- **Bloom** post-processing for the glowing look.
- Draw potentials / walls directly on the canvas.

### Notes
This is a separate lineage from the *light-transport* project: light-transport traces rays, WAVE FIELD integrates the field itself.

---

## 日本語

量子（シュレーディンガー方程式・Visscher 実部/虚部リープフロッグ法）と古典（スカラー波動方程式）の
**2エンジン**波動場シミュレータ。WebGL2 単一 HTML で完結。同じジオメトリを通して、確率振幅と古典場が
どう伝播するかを見比べられる。

### 起動
```sh
cd ~/dev/wave-field
python3 -m http.server 8180
# → http://localhost:8180/
```

### 特徴
- **量子エンジン** — Visscher の実部/虚部スタガード更新でシュレーディンガー方程式を安定・ノルム保存で積分。
- **古典エンジン** — 同一格子上の2次スカラー波動方程式。
- **プリセット** — 二重スリット / 単スリット / 障壁・トンネル効果 / 自由波束 ほか。
- **波源** — ガウス波束の注入、または**マイク入力**で場を駆動。
- 発光感を出す **bloom** ポストプロセス。
- キャンバス上に直接ポテンシャル／壁を描画可能。

### 補足
光路を追う *light-transport* とは別系統で、こちらは「波の場」そのものを積分する。
