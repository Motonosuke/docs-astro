---
layout: ~/layouts/MainLayout.astro
title: コンテンツの執筆
description:  Astroは、ブログ、マーケティングサイト、ポートフォリオなど、コンテンツに特化したサイトに最適です。プロジェクト内で直接コンテンツを執筆することも、お好みのCMSを接続することも可能です。
i18nReady: true
---

Astroは、ブログ、マーケティングサイト、ポートフォリオなど、コンテンツに特化したサイトに最適です。

Astroは、コンテンツの執筆と見栄えの手伝いをします。Markdown/MDXを使ってAstroで直接ブログ記事を書いたり、ヘッドレスCMSからコンテンツを取得することができます。ページにレイアウトを追加したり、記事のインデックスを作成したり、読者が購読できるようにRSSフィードを設定したりすることができます。

## 執筆内容

Astroでは、さまざまな方法でコンテンツを執筆することができます。
- Markdownファイル(`.md`または[代替拡張子](/ja/guides/markdown-content/))では、リッチテキストを簡単に記述できるように設計されています。
- MDX (`.mdx`) ファイルでは、ドキュメントにコンポーネントや動的表現を含めることができます。
- サードパーティのコンテンツマネジメントシステム（CMS）を使用して、そのコンテンツを`.astro`ページに取り込みます。
- その他のオプションとして、[`.astro`ファイル](/ja/core-concepts/astro-pages/#astro-pages) や [`.html`ファイル](/ja/core-concepts/astro-pages/#html-pages) もあります（コンテンツが多いページではあまり使われません）。

### Markdownのオーサリング
Markdownは、基本的なフォーマットとヘッダー、リスト、画像などの一般的な要素を含むリッチテキストを書くための便利な構文です。Astroには、プロジェクト内のMarkdownファイルをサポートする機能が組み込まれています。

コードエディタで新しい`.md`ファイルを作成して書くか、お気に入りのMarkdownエディタで書かれた既存のファイルを持ち込んでください。[StackEdit](https://stackedit.io/)や[Dillinger](https://dillinger.io) などのオンラインMarkdown エディタでは、GitHubに保存されているAstroリポジトリと編集・同期することも可能です。

📚「AstroでMarkdownコンテンツを書く」(/ja/guides/markdown-content/)について詳しく説明します。

### MDXのオーサリング
MDXインテグレーションをプロジェクトに追加すると、`.mdx` ファイルを使用してコンテンツを記述することもできます。このファイルにより、JavaScript式やカスタムコンポーネントをMarkdownに含めることができます。これには静的な[Astro components](/ja/core-concepts/astro-components/)とインタラクティブな[framework components](/ja/core-concepts/framework-components/) の両方が含まれます。バナーやインタラクティブなカルーセルなどのUI要素をテキスト内に追加して、コンテンツを本格的なウェブページにすることができます。

プロジェクトファイルと一緒に、コードエディタで `.mdx` ファイルを直接書き、編集することができます。

📚 [AstroでMDXを使う](/ja/guides/integrations-guide/mdx/)の詳細はこちらです。

### ヘッドレスCMSオーサリング

Storyblok、WordPress、Contentfulなど、既存のコンテンツ管理システム（CMS）でブログ記事を書きます。Storyblokのような一部のCMSは、公式の[Astroインテグレーション](https://www.storyblok.com/mp/announcing-storyblok-astro)を提供しています。また、Astroページが[リモートコンテンツの取得](/ja/guides/data-fetching/#fetch from-a-headless-cms) に使用できるJavaScript SDKを公開しているものもあります。

## コンテンツページの管理

`src/pages`ディレクトリにあるMarkdownとMDXファイルは、Astroの[file-based routing](/ja/core-concepts/routing/) を使ってサイト上にページを自動生成し、投稿ファイルのパスに対応するURLに構築されます。

また、MarkdownやMDXファイルを`src/pages`ディレクトリの外に置いて、代わりに`.astro`ページに[その内容をインポートする](/ja/guides/markdown-content/#importing-markdown) ということも可能です。

CMSでコンテンツを書いている場合、投稿を取得して[ダイナミックルーティング](/ja/core-concepts/routing/#dynamic-routes)を使用すると、1つの `.astro` ファイルを使って、各投稿のルートを生成することが可能です。Astroのデフォルトの静的モードでは、これらのルートはビルド時に生成されます。SSRモード](/ja/guides/server-side-rendering/)にオプトインすると、実行時にリクエストに応答して、必要に応じてコンテンツを取得します。

## コンテンツを紹介する

ブログのアーカイブやブログのタグごとのページなど、コンテンツを整理して表示するための共通機能を構築するために、AstroではMarkdownやMDXのフロントマターから[ファイル名とメタデータを取得]（/en/reference/api-reference/#astroglob）してこれらを利用してページコンテンツやルートを生成することができます。

## コミュニティとの連携

公式の [`@astrojs/mdx`](/en/guides/integrations-guide/mdx/) インテグレーションに加えて、Astroプロジェクトでコンテンツを扱うためのサードパーティ製の [community integrations](https://astro.build/integrations/css+ui/?q=content) が複数用意されています。
