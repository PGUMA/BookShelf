# 演習で慣れる！データベース

**三層スキーマ**

- 外部スキーマ
    外部で表示したり視認されるデータ構造のあり方(viewや結合結果)
- 概念スキーマ
    DB上での論理的なデータ構造のあり方（tableや関連）
- 内部スキーマ
    DBMS内部での物理的なデータ配置やあり方

# ゼロから学ぶTerraform

TODO

# エンジニアのための英語

## commit logの書き方

### commit区分

- 修正

    `fix`

    > fix (for) ~

- 追加

    `add`

    > add ~

- 削除

    `remove/delete`

    > remove/delete ~

- リファクタリング

    `refactor`

    > refactor ~

- 移動

    `move`

    > move ~ to/in ~

- 変更

    `change`

    > change ~ to/for ~

- 改善

    `improve`

    > improve ~

#### 内容表現

- 〜にする

    `make`

    > make ~ ~

- 使う

    `use`

    > use ~

- 許容

    `allow`

    > allow ~

- しない

    `don't`

    > don't ~

# コンポーネント駆動開発

ページベース開発→コンポーネント駆動開発（CDD）

**コンポーネントとは？**

    UIを構築するモジュラーな部品

**コンポーネント駆動開発**

    近年の複雑化するアプリケーションUIへの要求に対して高い凝集性/低い結合度を保ち保守性を高めるための開発アプローチ
    ※UIをモジュール化して汎用性を高めて適切に再利用できる環境が必要

## サポートツール

UIコンポーネントエクスプローラー

デファクトスタンダード = Stroybook

**Stroyとは**

    Stroybookに登録したコンポーネントに対して、特定状態を与えたもの

### 環境構築

[参考](https://storybook.js.org/docs/react/get-started/install)
```
npx create-react-app sb-ts-react-playground --template typescript
cd <app-name>
npx -p @storybook/cli sb init --use-npm
npm run storybook
```

> ※2020/04/27時点でnode@18には対応できていない[^1]模様(node@17.9.0)にて起動確認

[^1]: https://github.com/storybookjs/storybook/issues/18010


### 機能

**CSF3.0**

※2021/11~の新機能

- title設定がデフォルトで自動付与されるように
    - プロジェクト内の命名規則が統一される
    - ディレクトリ配置の変更が自動で追従される
- object形式でexport可能に
- 上記objectを分割代入形式で再利用可能に

- play function
    - ユーザー操作をコード化して、操作によってのみ到達可能な状態をStorybook上で表現できる
    - テストコードとして再利用可能（ex Jestと連携）

[参考URL](https://github.com/takefumi-yoshii/wdb-frontendcsf-play-example)