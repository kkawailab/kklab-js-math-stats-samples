# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

JupyterLite JavaScript カーネル対応の数学・統計学チュートリアル。mathjs と simple-statistics ライブラリを使用した教育用 Jupyter ノートブック集。

## Architecture

- **notebooks/**: 全6章の `.ipynb` ファイル（01〜06の連番）
- ノートブックは JupyterLite の JavaScript カーネルで実行
- 外部ライブラリは ESM として CDN (esm.sh) から動的インポート

## Library Versions

ノートブック内で使用するライブラリのインポート形式:

```javascript
const math = await import('https://esm.sh/mathjs@13.0.0');
const ss = await import('https://esm.sh/simple-statistics@7.8.8');
```

## Notebook Structure

各ノートブックは以下の構成:
1. タイトルと学習目標（Markdown）
2. ライブラリ読み込みセル
3. セクションごとの解説と実行可能コード
4. 実践例
5. 練習問題（空のコードセル付き）

## Content Guidelines

- 日本語で解説
- 数学的概念は段階的に説明
- コード出力は `console.log()` で表示
- 練習問題のコードセルはコメント「// ここに回答を書いてください」で開始
