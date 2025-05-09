# 時系列予測による変圧器の保護  
Transformer Oil‑Temperature Forecasting with LightGBM

## プロジェクト概要
油入り変圧器は負荷変動に応じて発熱し、油温（OT: Oil Temperature）が上昇します。  
冷却装置の運転を経験則ではなく **24 時間先の油温予測** に基づいて最適化し、  
設備劣化と電力消費を同時に抑えることを目的としとしたプロジェクトです。

## ディレクトリ構成
├── src/                      ← メインのコード
│   ├── __init__.py
│   ├── data_loader.py        ← データ読み込み・前処理
│   ├── feature_engineering.py← 特徴量生成
│   ├── model.py              ← モデル構築・学習
│   ├── train.py              ← 学習実行スクリプト
