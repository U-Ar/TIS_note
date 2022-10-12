Transactional Information Systems 読書ノート
===

Transactional Information Systemsに関する読書ノートをまとめたブック。場合によっては日本語要約としての役割も果たせると思うので公開する。

もっとさっぱり読書感想をまとめたブログエントリは https://u-ar.hatenablog.com/entry/bookmemo5 にある。

一部重要な演習問題の解答(MVCCアルゴリズム群の正当性の証明など)は本ノートの付加価値として掲載している。~~載ってないものは、手書きで紙のノートに書きなぐり、電子の海に移し替える気力を持たなかったものたち。~~

第1部 導入
---

- [1章-1 イントロ、及びハードウェアのさらっとした説明](/9EbzCQMpShyTvHjrmTEBEg)
- [2章-1 ページモデル/オブジェクトモデルの定義](/VgxvykwHSTeAmug4rV-HNw)

第2部 Concurrency Control
---

- 3章：Serializability (逐次実行可能性)の定式化
    - [3章-1 スケジュールの構文論/意味論的定義](/gX6cYQtnQuCPWgSDAgT5Sw)
    - [3章-2 基礎的なSerializability](/ZJZqUsTVQH6aSUV5GvHtlQ)
    - [3章-3 中断を考慮した/分離性を柔軟にしたSerializability](/-rYtcHUkRSmjZ-uClCNkuw)

- 4章：Concurrency Controlアルゴリズム
    - [4章-1 Concurrency Control アルゴリズム](/Gxz1byDJSaiL3UuhGt4Vtw)
    - [4章-2 ロックスケジューラ](/bASQ7zDETWObl-LyK5bUuQ)
    - [4章-3 ロックを用いないスケジューラ](/5yyJyTNnQi-z7GdAcATBzg)
    - [4章-4 ハイブリッドスケジューラ](/JXVEqjvSRlqIc9zmhHWP0A)
    - 解けてない演習問題: 4.3 4.10　怪しい: 4.18

- 5章：Multiversion Concurrency Control
    - [5章-1 Multiversion Serializability](/MsKUab9GQKyp0s6hBePJFQ)
    - [5章-2 Multiversion CC](/Xyyfbhr5S_C8qjX8Jas-tA)
    - no blind writeでMVSR=MCSR, actionでVSR=MVSRが怪しい

- 6章：Object Model における Serializability
    - [6章-1 Object Modelの導入](/Hh8CjFEfRCmoB97LpkZc1A)

- 7章：Object Model における Concurrency Control
    - [7章-1 CC on Objects](/QTQf4ryjTMqOrSJafCyjUQ)

- 8章：Relational Database における Concurrency Control
    - [8章-1 RDBにおけるConcurrency Control](/aeTOJ0wAQqGpWmlBA92jJA)





訳について
---

訳はすべて我流。最初に充てた単語を一貫性のために最後まで使い続けているので、後から振り返ると怪しいのが多い。

- reducibilityを「削減可能性」と訳したが、帰着可能性とか整理可能性とかの方が(serialなスケジュールに整理するという文脈で)正確と思われる。
- conflictはトランザクション間については「衝突」、ロック間については「競合」としたが、競合に統一しても良かったと思う(衝突だと物理的なイメージが強すぎる)。
- serializabilityは日本語にしづらすぎて最後まで英語のままにした。強いて訳すなら、一つ一つ実行する場合と等価というニュアンスを勘案して「逐次実行可能性」などになるだろうか。



