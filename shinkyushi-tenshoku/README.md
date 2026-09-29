# 国試黒本治療家エージェント 審査用LP（鍼灸割合）

- 台本（正本）: `kkeisuke0407-crypto/hozon` の `案件_国試黒本治療家エージェント/04_審査用LP_鍼灸割合_v7_パーツ配置版.md`（本文はv6のまま、パーツ配置をv7で指定）
- パーツ: `hozon/LPパーツ集_体験談ランキング型/`（44パーツ版・mt-*）
- 対象: スマートフォン（375px基準）
- 用途: A8/広告主審査提出用・Google検索広告用（Base KW: 鍼灸師 転職）
- サイト名: 治療家キャリアノート（https://chiryoka.hakobu-family.com/ 、GitHub Pages。ルート `/` はこのLPへ転送）
- 公開URL: https://chiryoka.hakobu-family.com/shinkyushi-tenshoku/
- サイト共通: `../site.css`（ページ枠・サイト名の帯・フッター）、`../operator/`（運営者情報）、`../privacy/`（プライバシーポリシー）、`../disclosure/`（広告掲載について）

| ファイル | 中身 |
|---|---|
| `index.html` | 本文。FV以外はすべて mt-* パーツ |
| `parts.css` | パーツ集の `parts.css` を**無改変**でコピー（44パーツ版） |
| `style.css` | ページ枠（見本ページと同じ `mt-wrap` / `mt-figure`）、改行の調整（`lp-nw`＝語句の途中で切らない）、v7で専用指定のFV、中央寄せ強調、主CTAの見出し1行 |
| `images/fv-hero.webp` | FV背景。考える鍼灸師の画像（1400×788）。スマホもPCも元の16:9のまま表示し、左の明るい部分に文字を重ねる（文字サイズだけ画面幅に合わせる） |
| `images/kurohon-banner.webp` | 国試黒本治療家エージェントの公式バナー（600×500）。`mt-banner` でPR表記つき |
| `images/shinkyushi-nayami.webp` | SECTION1 の大見出しの直下の挿絵「もっと鍼を打てる職場がいいかも…」（900×675） |
| `images/talk-a.webp` / `talk-b.webp` | 会話のアイコン（240×240）。A＝考える女性（hozon バックアップのクボタLP `thinking-woman-v1.webp` から顔を切り出し）、B＝男性（同 時計査定LP `avatar-1.png`） |
| `images/training-time.webp` | 画像v9。SECTION1「④ 勉強会・研修の時間帯」の本文直後（1536×1024） |
| `images/workplace-choice-a.webp` | 画像v9。SECTION3 のH2直下（mt-worryの前）＋「※画像はイメージです。」（1536×1024） |
| `images/five-reasons.webp` | 画像v9。SECTION4 のH2直下（①の前）（1536×1024） |
| `images/summary-checkpoints.webp` | 画像v9。SECTION7「まとめ」のH2直下、結論ボックスの前（1536×1024） |
| `images/kyujin-3rei.webp` | SECTION2 求人例A/B/Cの比較画像（1200×675）。タップで拡大表示 |

## 公開前にやること

1. `index.html` 末尾の `CTA_URL` にアフィリエイトリンクを入れる（ボタン・テキストリンク・追従ボタンすべてに反映）。
2. 審査・出稿時は `<meta name="robots" content="noindex, nofollow">` の要否を確認する。

## v7の配置どおりの対応

| v7の指示 | 実装 |
|---|---|
| 0. PR帯 | `mt-prbar`（更新日 2026年9月28日） |
| 1. FV | 専用ヒーロー（背景画像＋HTMLテキスト、「ちゃんと鍼を打てる職場」を最大）。CTAは置かない。画像は16:9のまま拡大しない |
| 2. 会話 | `mt-talk`（右・ピンク＝Aさん〔悩む女性〕／左・青＝担当者〔男性・エージェント風に回答〕、4吹き出し、黄マーカーは答えの予告1か所）→ `mt-oneline`「中身はかなり違う。」 |
| 3. 早期CTA | `mt-cta`（`#cta-early`）。ここを過ぎたら `mt-sticky` を表示 |
| 4. 4つの中身 | 大見出しの直下に挿絵 → `mt-check` で4項目 → 各項目 `mt-h4`＋本文（①の読者の本音は `mt-say`）→ 中央寄せ強調 |
| 5. 求人3例 | `mt-h3`「編集部が注目した治療家向け求人サービスを見てみると…？」＋導入2行（サービス名は mt-bridge まで出さない）→ 比較画像1枚 ＋ `mt-small` ＋ `mt-conclusion`（HTMLのカードは使わない） |
| 6. 中間CTA | `mt-textlink` |
| 7. 自分で比べるのは大変 | `mt-worry` ＋ 本文 ＋ 普通のul →「実は、こうした細かい条件まで見ながら探せるサービスがあります。」→ `mt-bridge`（編集部が注目したのが、＼サービス名／）→ 公式バナー `mt-banner` → `mt-spec`（おすすめポイント3つ＋公式サイトボタンのみ。評価表はSECTION4と重複するため削除） |
| 8. 5つの強み | ①本文 ②本文＋ul＋`mt-info--tip`（電球：相談するときの伝え方）③`mt-points` ④`mt-oneline`＋本文＋`mt-info`（非公開求人とは？）⑤本文 → `mt-check`「こんな人におすすめ」。各項目は公式サイトで確認できた事実で補強 |
| 9. 主CTA | `mt-cta` ＋ 見出し1行「希望条件を無料で相談」 |
| 10. 口コミ | `mt-h3` のリード → 口コミカード `mt-review`×3（元の体験談に評価が無いので星なし。ポイントは本文内 `mt-mark`）→ `mt-small` |
| 11. 口コミ後CTA | `mt-textlink` |
| 12. 運営面 | 本文 ＋ `mt-check` |
| 13. まとめ | `mt-conclusion`（見出し＋ul＋`mt-mark` 1か所） |
| 14. 最終CTA | `mt-cta` ＋ 注記 `mt-small` |

## v7と違うところ・判断したところ

- 強み①〜⑤の見出しは5つとも `mt-h3`（v7の本文では②⑤が `mt-h4` だが、v7の使用回数表「mt-h3＝サービス訴求の大項目／mt-h4＝ジャンル知識の4項目」に合わせた）。
- `mt-sticky` のscriptは、監視対象を早期CTA（`#cta-early`）にしている（v7「早期CTA通過後から表示」）。
- 追従ボタンのひとことは「＼希望条件を無料で相談／」（v6本文の文言）。
- 口コミ後のテキストリンクの注記は「└希望条件を無料で相談する」（v6のボタン文言）。
- 画像v9（`hozon/案件_国試黒本治療家エージェント/06_画像設計_v9/CLAUDE_実装指示.md`）：4枚（training-time・workplace-choice-a・five-reasons・summary-checkpoints）を配置済み。hozon のZIPは途中で切れていたため、画像はチャットで受け取ったものを使用。
- 広告主の訴求の補強は、公式サイト（kurohon.jp/agent・/agent/service・/agent/staff）、運営会社のプレスリリース（2025年4月3日）、公式バナーで確認できたものだけ。他社LPにある「業界No.1」「求人3,000件以上」「年収50万円以上アップ」「LINE相談」「条件交渉力」「しつこい電話なし」は公式で確認できないため入れていない。
- `mt-check` は台本v7の目安（2回）を超えて3回（4つの中身／こんな人におすすめ／運営面）。
- 会話のBさんは、指示により男性のエージェント風（表示名「担当者」）として敬語で答える形に書き換え。Aさんも相手に合わせて敬語に。内容（給与・休日→鍼を打てない職場→施術内容は分からない→鍼灸割合で比べる）は台本どおり。
- FVコピーを「次の転職先、『ちゃんと鍼を打てる職場』ですか？」に変更（指示による）。求人3例の導入はサービス名を出さない形に変更。
- 品質修正（`hozon/案件_国試黒本治療家エージェント/08_品質修正_Claude指示.md`）を反映：SECTION2の導入、SECTION3のサービス名初公開の流れ、公開直後の説明を3点に軽量化、旧サービス名（名称変更）の説明と「評価は編集部の主観」の注記を削除。早期CTAは変更なし。
