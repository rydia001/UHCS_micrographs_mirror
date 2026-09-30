# UHCS micrographs mirror

[![DOI](https://zenodo.org/badge/1376795207.svg)](https://doi.org/10.5281/zenodo.23050463)

超高炭素鋼（ultrahigh carbon steel）の SEM 像データセットのミラー。

## なぜミラーか

オリジナルの配布元 `https://hdl.handle.net/11256/940`（NIST materialsdata）は
2026 年 9 月時点で応答せず、公開当時の探索サイト `uhcsdb.materials.cmu.edu` も
接続できない。データ自体は Internet Archive に残っているが、ファイルごとに保存時刻が
異なるうえ取得が不安定なため、再配布が許されている条件（CC BY 3.0 US）のもとで複製した。

## 内容

| パス | 内容 |
|---|---|
| `micrographs/` | SEM 像 961 枚（TIFF と PNG の混在） |
| `metadata.csv` | 画像 961 件のメタデータ。組織ラベル、検出器、倍率、スケールバー、試料 ID、焼鈍温度・時間、冷却方法 |
| `manifest.json` | 全ファイルの sha256 |
| `provenance/` | ライセンス表示の根拠（オリジナルの配布ページのスナップショット） |

`metadata.csv` の `path` 列が `micrographs/` 以下のファイル名に対応する。

## ライセンスと引用

Creative Commons Attribution 3.0 United States (CC BY 3.0 US)（https://creativecommons.org/licenses/by/3.0/us/）。利用時は次を引用すること。

> B. L. DeCost, M. D. Hecht, T. Francis, B. A. Webler, Y. N. Picard, E. A. Holm, UHCSDB: UltraHigh Carbon Steel Micrograph DataBase, Integrating Materials and Manufacturing Innovation 6, 197-205 (2017). doi:10.1007/s40192-017-0097-0

このミラー自体は Zenodo に版ごとに保管してある（全版: doi:10.5281/zenodo.23050463、v1.0.0: doi:10.5281/zenodo.23050464）。データを引用するときは上の論文を、入手経路を示すときはこの DOI を書く。

オリジナルの配布ページのスナップショット: https://web.archive.org/web/20230108232657/https://materialsdata.nist.gov/handle/11256/940

## 注意

- 画像 961 枚は試料 43 個から撮られている（1 試料あたり平均
  22 枚）。画像単位でランダムに訓練・テストへ分けると同一試料が
  両側に入り、性能を過大評価する。**試料単位（`sample_key`）で分けること。**
- 検出器は SE が 845 枚、BSE が 84 枚、記録なしが 32 枚。倍率は 42 通り。
- 焼鈍条件が記録されているのは 598 枚のみ。
