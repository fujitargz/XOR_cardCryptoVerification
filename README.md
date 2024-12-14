# XOR_cardCryptoVerification

SCIS2025

## 環境構築

検証の実行には[CBMC](https://www.cprover.org/cbmc/)が必要です。
[Installation](https://www.cprover.org/cprover-manual/installation/)に従いCBMCをインストールしてください。

## 実行方法

操作回数1回の不可能性を検証するコマンドは以下の通りです。

```sh
$ ./runTwoCard.sh 4 1 '-D WEAK_SECURITY=1' '-D FORCE_RANDOM_CUTS=1'
```

検証結果は本repositoryの`results/`に格納しています。

## 関連研究

検証プログラムは[mi-ki/cardCryptoVerification](https://github.com/mi-ki/cardCryptoVerification)をベースとして、
[fujitargz/fix-cardCryptoVerification](https://github.com/fujitargz/fix-cardCryptoVerification)によるプログラムの修正を適用し、
さらにXOR検証に対応するよう拡張したものです。