# 国試黒本治療家エージェント 審査用LP（鍼灸割合）

- 台本（正本）: `kkeisuke0407-crypto/hozon` の `案件_国試黒本治療家エージェント/04_審査用LP_鍼灸割合_v7_パーツ配置版.md`（本文はv6のまま、パーツ配置をv7で指定）
- パーツ: `hozon/LPパーツ集_体験談ランキング型/`（40パーツ版・mt-*）
- 対象: スマートフォン（375px基準）
- 用途: A8/広告主審査提出用・Google検索広告用（Base KW: 鍼灸師 転職）
- サイト名: 治療家キャリアノート（https://chiryoka.hakobu-family.com/ 、GitHub Pages。ルート `/` はこのLPへ転送）
- 公開URL: https://chiryoka.hakobu-family.com/shinkyushi-tenshoku/
- サイト共通: `../site.css`（ページ枠・サイト名の帯・フッター）、`../operator/`（運営者情報）、`../privacy/`（プライバシーポリシー）、`../disclosure/`（広告掲載について）

| ファイル | 中身 |
|---|---|
| `index.html` | 本文。FV以外はすべて mt-* パーツ |
| `parts.css` | パーツ集の `parts.css` を**無改変**でコピー（40パーツ版） |
| `style.css` | ページ枠（見本ページと同じ `mt-wrap` / `mt-figure`）、改行の調整（`lp-nw`＝語句の途中で切らない）、v7で専用指定のFV、中央寄せ強調、主CTAの見出し1行 |
| `images/fv-hero.webp` | FV背景。考える鍼灸師の画像（1400×788）。スマホは文字の下に人物、PCは左の余白に文字を重ねる |
| `images/shinkyushi-nayami.webp` | SECTION1 ①の後の挿絵「もっと鍼を打てる職場がいいかも…」（900×675） |
| `images/kyujin-3rei.webp` | SECTION2 求人例A/B/Cの比較画像（1200×675）。タップで拡大表示 |

## 公開前にやること

1. `index.html` 末尾の `CTA_URL` にアフィリエイトリンクを入れる（ボタン・テキストリンク・追従ボタンすべてに反映）。
2. 審査・出稿時は `<meta name="robots" content="noindex, nofollow">` の要否を確認する。

## v7の配置どおりの対応

| v7の指示 | 実装 |
|---|---|
| 0. PR帯 | `mt-prbar`（更新日 2026年9月28日） |
| 1. FV | 専用ヒーロー（背景画像＋HTMLテキスト、「どれくらい鍼を打てるか」を最大）。CTAは置かない |
| 2. 会話 | `mt-talk`（右＝Aさん／左＝Bさん、4吹き出し、黄マーカーは答えの予告1か所）→ `mt-oneline`「中身はかなり違う。」 |
| 3. 早期CTA | `mt-cta`（`#cta-early`）。ここを過ぎたら `mt-sticky` を表示 |
| 4. 4つの中身 | `mt-check` で4項目 → 各項目 `mt-h4`＋本文、①の後に挿絵 → 中央寄せ強調 |
| 5. 求人3例 | 比較画像1枚 ＋ `mt-small` ＋ `mt-conclusion`（HTMLのカードは使わない） |
| 6. 中間CTA | `mt-textlink` |
| 7. 自分で比べるのは大変 | `mt-worry` ＋ 本文 ＋ 普通のul → `mt-bridge`（＼サービス名／） |
| 8. 5つの強み | ①本文 ②本文＋ul ③`mt-points` ④`mt-oneline`＋本文 ⑤本文 |
| 9. 主CTA | `mt-cta` ＋ 見出し1行「希望条件を無料で相談」 |
| 10. 口コミ | `mt-h3` のリード → `mt-story`×3（ポイントは本文内 `mt-mark`）→ `mt-small` |
| 11. 口コミ後CTA | `mt-textlink` |
| 12. 運営面 | 本文 ＋ `mt-check` |
| 13. まとめ | `mt-conclusion`（見出し＋ul＋`mt-mark` 1か所） |
| 14. 最終CTA | `mt-cta` ＋ 注記 `mt-small` |

## v7と違うところ・判断したところ

- 強み①〜⑤の見出しは5つとも `mt-h3`（v7の本文では②⑤が `mt-h4` だが、v7の使用回数表「mt-h3＝サービス訴求の大項目／mt-h4＝ジャンル知識の4項目」に合わせた）。
- `mt-sticky` のscriptは、監視対象を早期CTA（`#cta-early`）にしている（v7「早期CTA通過後から表示」）。
- 追従ボタンのひとことは「＼希望条件を無料で相談／」（v6本文の文言）。
- 口コミ後のテキストリンクの注記は「└希望条件を無料で相談する」（v6のボタン文言）。
- SECTION3（迷う鍼灸師）とSECTION4 ②付近（相談シーン）の挿絵は、画像が無いため未配置。
