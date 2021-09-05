## Gitなりすましの手順

![](https://i.imgur.com/IURFRMC.png)

1. `git clone`からの`git log`でcommitに紐づくメールアドレスを確認
2. `.gitconfig`の`user`ブロックの`email`を取得したアドレスに変更
3. ファイルに変更を加えてコミットする

## 対策
- GPGまたはS/MIMEを登録するの設定を行い、署名付きでコミットする
  - 署名設定後、GitHub上ではコミットに`Verified`タグがつくようになる
  - とはいえ、署名なしのコミットに関しては変わらず、同じアドレスでコミットできる。
    - 署名付きコミット → 本人であることの保証
    - 署名なしコミット → 本人かわからない（名乗っているだけ）

https://docs.github.com/ja/github/authenticating-to-github/managing-commit-signature-verification/signing-commits
