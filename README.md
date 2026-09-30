# 予想外のインフレと政府債務／円安で得をするのは誰か：再現パッケージ

SVillage（https://s-v.jp.net）の次の2本の記事で使った数値と図を再現するためのデータとノートブックです。

- 前編：予想外のインフレで誰が得をする？――政府債務と「見えない税」
- 後編：円安で得をするのは誰か――政府・企業・家計の海外資産

## 使い方

1. `svillage_unexpected_inflation_colab.ipynb` を Google Colab で開きます（GitHub上のファイルを開き、「Open in Colab」から開けます）。
2. 同じリポジトリにある `svillage_unexpected_inflation_colab_package.zip` をダウンロードし、最初のセルでアップロードします（中身は `data/` のCSVとノートブックです）。
3. 上から順に実行すると、記事の主な数値の一覧と、前編の図1〜5・後編の図1〜2が再現されます。

ローカルのJupyterで実行する場合は、リポジトリ直下で開けば `data/` をそのまま読み込みます。

## データ（`data/`）

2026年9月30日に一次ソースから取得したデータを、整形済みのCSVにしています。

| ファイル | 内容 | 出所 |
|---|---|---|
| 01_mitoshi_cpi_forecast.csv | 政府経済見通しの消費者物価（総合）見通し（年度、%） | 内閣府「政府経済見通し」各年度版（閣議決定） |
| 02_cpi_monthly.csv | 消費者物価指数 総合（月次、2025年=100） | 総務省「2025年基準消費者物価指数」長期時系列 |
| 03_jgb_general_bonds_balance.csv | 普通国債残高（年度末、兆円） | 財務省「最近20カ年間の年度末の国債残高の推移」 |
| 04_jgb_avg_coupon.csv | 普通国債の利率加重平均（年度末、%） | 財務省「普通国債の利率加重平均の各年ごとの推移」 |
| 05_nominal_gdp_fy.csv | 名目GDP（年度、兆円） | 内閣府「2026年4-6月期四半期別GDP速報（2次速報値）」 |
| 06_tax_revenue_fy.csv | 一般会計税収（年度、兆円） | 財務省「税収の推移」 |
| 07_wages_index_cy.csv | 名目・実質賃金指数（暦年、2020年=100） | 厚生労働省「毎月勤労統計調査」 |
| 08_primary_income_cy.csv | 第一次所得収支・直接投資収益・再投資収益（暦年、兆円） | 財務省「国際収支状況」 |
| 09_fx_reserves_usdjpy_monthly.csv | 外貨準備（金を除く、百万ドル）と円ドル相場（月次） | IMF・FRB（FRED: TRESEGJPM052N, EXJPUS） |
| 10_fof_household_quarterly_oku_yen.csv | 家計の金融資産の内訳（四半期末、億円） | 日本銀行「資金循環統計」 |

各データの取得元URLは、ノートブックの各セルのコメントに記載しています。

## English summary

Data and a Colab notebook that reproduce the figures and key numbers in two SVillage articles (in Japanese) on unexpected inflation and Japanese government debt, and on who benefits from the weak yen. All data were retrieved from official Japanese statistics (Cabinet Office, MIC, MOF, MHLW, Bank of Japan) and FRED on 30 September 2026.

© SVillage
