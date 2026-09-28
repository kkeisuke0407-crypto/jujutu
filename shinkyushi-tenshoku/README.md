# 国試黒本治療家エージェント 審査用LP（鍼灸割合）

- 台本（正本）: `kkeisuke0407-crypto/hozon` の `案件_国試黒本治療家エージェント/04_審査用LP_鍼灸割合_v6.md`
- パーツ: `hozon/LPパーツ集_体験談ランキング型/`（mt-*）をそのまま使用
- 対象: スマートフォン（375px基準）
- 用途: A8/広告主審査提出用・Google検索広告用（Base KW: 鍼灸師 転職）
- 公開URL: https://chiryoka.hakobu-family.com/shinkyushi-tenshoku/ （GitHub Pages。ルート `/` はここへ転送）

| ファイル | 中身 |
|---|---|
| `index.html` | 本文。すべて `mt-*` パーツで組んでいる |
| `parts.css` | パーツ集の `parts.css` を**無改変**でコピー |
| `style.css` | ページ枠（見本ページ k18-kihei-kaitori と同じ `mt-wrap` / `mt-title` / `mt-sitebar--foot`）と、FV背景画像の指定だけ |
| `images/fv-bg.webp` | FV背景。元画像（1916×821）を右寄せで16:10に切り出し、1200×750に縮小 |

## 公開前にやること

1. `index.html` 末尾の `CTA_URL` にアフィリエイトリンクを入れる（全CTAボタン6か所に反映）。
2. サイト名の帯（`mt-sitebar`）は仮で「鍼灸師の転職のえらび方」。実際のサイト名に差し替える。
3. 審査・出稿時は `<meta name="robots" content="noindex, nofollow">` の要否を確認する。

## パーツ対応

| 台本（v6） | パーツ |
|---|---|
| FV タイトル・画像 | `mt-title` ＋ `mt-eyecatch`（背景に施術室の画像） |
| PR表記 | `mt-small` |
| 会話 | `mt-chat`（2往復） |
| 結論ボックス | `mt-conclusion`（【結論】） |
| 各セクション見出し | `mt-h2` |
| 4つの中身・5つの強み・求人例 | `mt-h3` ＋ `mt-h4`（キーワード1つを赤マーカー） |
| 求人3例の比較 | `mt-hint` ＋ `mt-scroll` ＋ `mt-table` |
| 箇条書き | `mt-points` |
| 自分で比べる手間 | `mt-steps` |
| 「そこまで細かい希望を…？」 | `mt-worry` |
| 公式体験談の要約 | `mt-story` |
| 一番言いたい1行 | `mt-oneline` |
| CTA | `mt-cta`（＼ひとこと／＋ボタン＋注記） |

本文・数字・注記は台本から変えていない。台本にない文言は、パーツのルール上必要な次のものだけ。
- アイキャッチの吹き出し「鍼灸割合、見てる…？」
- FVのCTAのひとこと「＼施術内容の中身まで見て選ぶ／」（FV本文から引用）
- 会話の見出し「▼Aさん（左）とBさん（右）の会話」
- 冒頭のPR表記「※本ページにはプロモーションが含まれています。」
- 表の上下の「表は横にスクロール可能」、結論ボックスの「【結論】」
