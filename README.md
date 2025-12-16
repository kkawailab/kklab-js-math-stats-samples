# JavaScript 数学・統計学チュートリアル

JupyterLite の JavaScript カーネルで動作する、数学と統計学の包括的なチュートリアルです。

## 概要

このリポジトリは、[mathjs](https://mathjs.org/) と [simple-statistics](https://simple-statistics.github.io/) ライブラリを使用して、初歩レベルから高度なレベルまでの数学および統計学を学ぶための教材を提供します。

### 特徴

- **ブラウザで動作**: JupyterLite を使用してサーバー不要で実行可能
- **インタラクティブ**: 実際にコードを実行しながら学習
- **段階的な学習**: 基礎から応用まで体系的にカバー
- **実践的な例題**: 各章に練習問題を収録

### 使用ライブラリ

| ライブラリ | バージョン | 用途 |
|------------|------------|------|
| [mathjs](https://mathjs.org/) | 13.0.0 | 数学計算、線形代数 |
| [simple-statistics](https://simple-statistics.github.io/) | 7.8.8 | 統計計算、回帰分析 |

## 目次

### 第1章: 環境セットアップと基礎
**ファイル**: [`notebooks/01_introduction.ipynb`](notebooks/01_introduction.ipynb)

- 1.1 ライブラリの読み込み
- 1.2 mathjs の基本操作
  - 四則演算、数学関数、三角関数、数式パーサー、定数
- 1.3 simple-statistics の基本操作
  - 基本的な統計量、散布度、パーセンタイル
- 1.4 実践例: データ分析の基本フロー
- 1.5 練習問題

### 第2章: 線形代数
**ファイル**: [`notebooks/02_linear_algebra.ipynb`](notebooks/02_linear_algebra.ipynb)

- 2.1 ベクトル
  - 作成、基本演算、内積・外積、ノルム、角度
- 2.2 行列
  - 作成、特殊行列、基本演算、積、転置
- 2.3 連立方程式の解法
  - 逆行列法、LU分解
- 2.4 行列の分解
  - LU分解、QR分解
- 2.5 固有値と固有ベクトル
- 2.6 実践例: 主成分分析（PCA）の基礎
- 2.7 練習問題

### 第3章: 統計学基礎
**ファイル**: [`notebooks/03_statistics_basics.ipynb`](notebooks/03_statistics_basics.ipynb)

- 3.1 データの種類
- 3.2 代表値（中心傾向の指標）
  - 算術平均、中央値、最頻値、幾何平均、調和平均、トリム平均
- 3.3 散布度（ばらつきの指標）
  - 範囲、分散、標準偏差、四分位範囲、変動係数
- 3.4 分布の形状
  - 歪度、尖度
- 3.5 相関分析
  - 共分散、ピアソンの相関係数、決定係数
- 3.6 データの標準化
  - Zスコア、偏差値、Min-Max正規化
- 3.7 実践例: クラスの成績分析
- 3.8 練習問題

### 第4章: 確率分布
**ファイル**: [`notebooks/04_probability_distributions.ipynb`](notebooks/04_probability_distributions.ipynb)

- 4.1 確率の基本
  - 基本概念、条件付き確率、ベイズの定理、組み合わせ・順列
- 4.2 離散確率分布
  - 二項分布、ポアソン分布
- 4.3 連続確率分布
  - 正規分布、t分布、カイ二乗分布
- 4.4 中心極限定理
- 4.5 simple-statisticsの確率関数
- 4.6 実践例: 信頼区間の計算
- 4.7 練習問題

### 第5章: 回帰分析
**ファイル**: [`notebooks/05_regression_analysis.ipynb`](notebooks/05_regression_analysis.ipynb)

- 5.1 単回帰分析
  - 最小二乗法の原理、計算過程、予測値
- 5.2 回帰モデルの評価
  - 決定係数（R²）、自由度調整済みR²、標準誤差
- 5.3 重回帰分析
- 5.4 多項式回帰
- 5.5 指数回帰と対数回帰
- 5.6 ロバスト回帰（Theil-Sen推定）
- 5.7 実践例: 売上予測モデル
- 5.8 練習問題

### 第6章: 高度な統計解析
**ファイル**: [`notebooks/06_advanced_statistics.ipynb`](notebooks/06_advanced_statistics.ipynb)

- 6.1 仮説検定の基礎
  - 仮説検定の考え方、z検定
- 6.2 t検定
  - 1標本t検定、2標本t検定、対応のあるt検定
- 6.3 カイ二乗検定
  - 適合度検定、独立性の検定
- 6.4 ベイズ分類器
- 6.5 k-means クラスタリング
- 6.6 時系列分析の基礎
  - 移動平均、指数移動平均、トレンド分析
- 6.7 実践例: A/Bテスト
- 6.8 練習問題

## 使い方

### JupyterLite で実行

1. JupyterLite（https://jupyterlite.readthedocs.io/）を起動
2. JavaScript カーネルを選択
3. ノートブックファイル（.ipynb）をアップロード
4. セルを順番に実行

### ライブラリの読み込み

各ノートブックの冒頭で以下のようにライブラリを読み込みます：

```javascript
// mathjs の読み込み
const math = await import('https://esm.sh/mathjs@13.0.0');

// simple-statistics の読み込み
const ss = await import('https://esm.sh/simple-statistics@7.8.8');
```

## 前提知識

- 基本的な JavaScript の知識
- 高校数学レベルの基礎知識（推奨）

## ファイル構成

```
kklab-js-math-stats-samples/
├── README.md                              # このファイル
└── notebooks/
    ├── 01_introduction.ipynb              # 第1章: 環境セットアップと基礎
    ├── 02_linear_algebra.ipynb            # 第2章: 線形代数
    ├── 03_statistics_basics.ipynb         # 第3章: 統計学基礎
    ├── 04_probability_distributions.ipynb # 第4章: 確率分布
    ├── 05_regression_analysis.ipynb       # 第5章: 回帰分析
    └── 06_advanced_statistics.ipynb       # 第6章: 高度な統計解析
```

## 参考リンク

- [mathjs 公式ドキュメント](https://mathjs.org/docs/)
- [simple-statistics 公式ドキュメント](https://simple-statistics.github.io/)
- [JupyterLite ドキュメント](https://jupyterlite.readthedocs.io/en/stable/)

## 更新履歴

### v1.0.0 (2025-12-16)
- 初版リリース
- 全6章のチュートリアルノートブックを作成
  - 第1章: 環境セットアップと基礎
  - 第2章: 線形代数
  - 第3章: 統計学基礎
  - 第4章: 確率分布
  - 第5章: 回帰分析
  - 第6章: 高度な統計解析

## ライセンス

MIT License

## 貢献

Issue や Pull Request を歓迎します。
