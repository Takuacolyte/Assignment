# 時系列予測による変圧器の保護  
Transformer Oil‑Temperature Forecasting with LightGBM

## 📖 プロジェクト概要
油入り変圧器は負荷変動に応じて発熱し、油温（OT: Oil Temperature）が上昇します。  
冷却装置の運転を経験則ではなく **24 時間先の油温予測** に基づいて最適化し、  
設備劣化と電力消費を同時に抑えることを目的としたプロジェクトです。

---

## 🔧 使用技術
| カテゴリ | ツール / ライブラリ |
|----------|-------------------|
| 言語      | Python 3.9+        |
| 主要ライブラリ | LightGBM, Optuna |
| データ処理 | Pandas, NumPy     |
| 可視化    | Matplotlib        |
| 評価指標  | MAE, Max Error     |

---

## 🗂️ ディレクトリ構成
❯ tree -a -I "node_modules|.next|.git|.pytest_cache|static" -L 2
.
├── src/ # モデル・前処理スクリプト
│ ├── data_loader.py
│ ├── feature_engineering.py
│ ├── train.py # LightGBM 学習 & ハイパーパラメーター探索
│ └── predict.py # 24h 先予測
├── data/
│ └── ett_small.csv # ETT-small などを配置
├── tests/ # pytest 等 (任意)
├── requirements.txt
└── README.md
