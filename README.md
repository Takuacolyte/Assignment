# 時系列予測による変圧器の保護  
Transformer Oil‑Temperature Forecasting with LightGBM

## 📖 プロジェクト概要
油入り変圧器は負荷変動に応じて発熱し、油温（OT: Oil Temperature）が上昇します。  
冷却装置の運転を経験則ではなく **24 時間先の油温予測** に基づいて最適化し、  
設備劣化と電力消費を同時に抑えることを目的としたプロジェクトです。

---

## 🔧 使用技術
| カテゴリ | ツール / ライブラリ | 備考 |
|----------|-------------------|------|
| 言語      | Python 3.9+        | 公式サポート LTS |
| 主要ライブラリ | LightGBM, Optuna | 勾配ブースティング & HPO |
| データ処理 | Pandas, NumPy     | 時系列前処理 |
| 可視化    | Matplotlib        | STL 分解など |
| 評価指標  | MAE, Max Error     | 平均絶対誤差・最大誤差 |:contentReference[oaicite:2]{index=2}:contentReference[oaicite:3]{index=3}

---

## 🗂️ ディレクトリ構成（例）
athena-assignment/
├── src/ # モデル・前処理スクリプト
│ ├── data_loader.py
│ ├── feature_engineering.py
│ ├── train.py # LightGBM 学習 & Optuna HPO
│ └── predict.py # 24h 先予測
├── data/
│ └── ett_small.csv # ETT-small などを配置
├── tests/ # pytest 等 (任意)
├── requirements.txt
└── README.md
