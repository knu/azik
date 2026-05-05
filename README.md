# 私の改造版AZIK設定

- ATOK用
    - ATOK for Mac向けに、ローマ字テーブルをインポート・エクスポート・差分表示するツール `bin/atok-romaji-table` を添付しています。（Windows版には対応していません）

      ```sh
      # 現在のATOKスタイルにテキストファイルをインポート
      bin/atok-romaji-table import atok-romantable-knu-azik.txt

      # 書き換えずにインポート結果のみを確認
      bin/atok-romaji-table import --check atok-romantable-knu-azik.txt

      # テキストファイルと現在のATOKスタイルの内容を比較
      bin/atok-romaji-table diff atok-romantable-knu-azik.txt

      # 現在のATOKスタイルからテキストファイルにエクスポート
      bin/atok-romaji-table export exported.txt
      ```

      対象のplistファイルは、テキストファイルの後ろに続けて指定できます。省略した場合は `~/Library/Preferences/ATOK*/Styles/StUser0.plist` のうち最新のATOKバージョンのものが対象になります。
      複数のスタイルを管理していて、StUser0.plist以外を対象にしたい場合は明示的に指定してください。

      **注意:** インポートはplistを直接書き換えます。万一に備え、対象のplistのバックアップを取っておくことを強くおすすめします。

- Google日本語入力用
    - こちらはふつうにインポート可能

## SEE ALSO

[AZIK総合解説書](http://hp.vector.co.jp/authors/VA002116/azik/azikinfo.htm)

## AUTHOR

Copyright (c) 2016-2026 Akinori MUSHA.

Licensed under the 2-clause BSD license.  See `LICENSE.txt` for
details.

Visit [GitHub Repository](https://github.com/knu/azik) for the latest
information.
