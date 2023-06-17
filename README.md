[![Orange banner indicating a preview software component][release-level-banner--unstable]](##)

<br />

<!-- markdownlint-disable-next-line line-length -->
<a href="##"><img src="https://raw.githubusercontent.com/OpenINF/openinf.github.io/live/assets/img/svg/logogram-color.svg?sanitize=true" alt="OpenINF logo" title="OpenINF" align="right" height="96" width="96" /></a>

<div align="left">

## `@openinf/util-text`

> Essential cross-platform terminal-friendly text utilities

<br />

[!['View on npm'][npm-badge--shields]][npm-badge-url]
[!['License: MIT/Apache-2.0'][license-badge--shields]][license-badge-url]

</div>

<br />

The high-level goal of `@openinf/util-text` is to serve as a Node.js package
containing **essential cross-platform text utilities** that degrade gracefully
when used in terminals lacking feature support. We are constantly working to
improve this repository, so please feel free to [contribute](#contributing) if
you notice any omissions or errors.

Thanks!

<br />

<details id="platform--node-js-lts">
	<summary>
		<a
			href="#platform--node-js-lts"
			title="Platform: Node.js LTS"
		>
			<img
				src="https://img.shields.io/badge/Node.js-LTS-black?logo=Node.js&logoColor=lightgreen&color=2a2a2a&labelColor=black"
				alt="Platform: Node.js LTS"
			/>
		</a>
	</summary>
	<div align="left"><br />
		<a
			target="_blank"
			title="Node.js release schedule"
			href="https://github.com/nodejs/release#release-schedule"
		>
			<strong>Supported Node.js Environments</strong>
		</a><br /><br />

- [ ] v4：Argon (Ar)
- [ ] v6：Boron (B)
- [ ] v8：Carbon (C)
- [ ] v10：Dubnium (Db)
- [ ] v12：Erbium (Er)
- [x] v14：Fermium (Fm)
- [x] v16：Gallium (Ga)
- [x] v18：Hydrogen (H)
<!-- TODO
- [x] v20: Iron (Fe) -->

</div></details>

<br />

<div align="center">

[![Code Style: Prettier][prettier-badge]][prettier-url]
[![Commit Style: Conventional Commits][conventional-commits-badge]][conventional-commits-url]
[![Chat on Matrix][matrix-badge--shields]][matrix-url]

</div>

<br /><br />

---

<br />

### Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API](#api)
- [Contributing](#contributing)
- [License](#license)

<br /><br />

---

<br />

<details>
<summary>
	<!-- markdownlint-disable-next-line line-length -->
	<h3 id="installation" align="left">Installation <a href="##"><img src="https://raw.githubusercontent.com/nodejs/corepack/main/icon.svg?sanitize=true" alt="Corepack logo" title="Corepack friendly" align="right" height="24" width="24" /></a></h3>
</summary>

<br />

`@openinf/util-text` runs on
[supported versions of Node.js](#platform--node-js-lts) and is available via
**`npm`**, **`pnpm`**, or **`yarn`**.

**Using the npm CLI**

<sup>See the
[official documentation for this command](https://docs.npmjs.com/cli/commands/npm-install)
for more information.</sup>

```shell
npm i @openinf/util-text
```

**Using the pnpm CLI**

<sup>See the [official documentation for this command](https://pnpm.io/cli/add)
for more information.</sup>

```shell
pnpm add @openinf/util-text
```

**Using the Yarn 1 CLI (Classic)**

<sup>See the
[official documentation for this command](https://classic.yarnpkg.com/en/docs/cli/add)
for more information.</sup>

```shell
yarn add @openinf/util-text
```

<br />

</details>

### Usage

To get started using the text utils provided by `@openinf/util-text`, all
that needs to be done is either import/require (depending on the module format)
the default export of the module or destructure the individual named helper
functions exported.

```ts
import { blueify, ellipsify } from '@openinf/util-text';

console.log(blueify(ellipsify('Deserializing database tables')));
```

<br /><br />

### API

<br />

<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OpenINF/GitHub-Markdown/HEAD/blockquotes/badge/light-theme/tip.svg">
  <img alt="Tip" src="https://raw.githubusercontent.com/OpenINF/GitHub-Markdown/HEAD/blockquotes/badge/dark-theme/tip.svg">
</picture><br />

The &ldquo;supplied string&rdquo; should be supplied by app developer (not arbitrarily)
because anything beyond that (e.g., in publicly-facing apps) may need be pre-processed.
The next release may perform preprocessing to follow Web Platform Design Principles.

<details>
<summary>
<a href="#" aria-controls="advanced-tips" aria-expanded="false"><h4 id="advanced-tips">Advanced Tips</h4></a>
</summary>

> - Speak with a diverse mix of prospective users within your target population
>   about your application and its intended purpose so as to get a wider
>   perspective on potential risks and adjust diversity criteria as needed.
> - The [AI Risk Management Framework][] released by the U.S. government's
>   National Institute of Standards and Technology (NIST) provides more detailed
>   guidance and additional learning resources for AI risk management.
> - DeepMind's publication on the [ethical and social risks of harm from LMs][]
>   describes in detail the ways that language model applications can cause
>   harm.
>
> &mdash; https://developers.generativeai.google/guide/safety_guidance#expandable-1

</details>

<br />

<dl>
<dt><a href="#blueify">blueify(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as blue colored if ANSI escapes are supported.</p>
</dd>
<dt><a href="#curlyQuote">curlyQuote(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as curly quoted if Unicode is supported.</p>
</dd>
<dt><a href="#ellipsify">ellipsify(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as ellipsified if Unicode is supported.</p>
</dd>
<dt><a href="#italicize">italicize(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as italicized if ANSI escapes are supported.</p>
</dd>
<dt><a href="#mdCodeSpans2html">mdCodeSpans2html(text)</a> ⇒ <code>string</code></dt>
<dd><p>Processes the supplied string by transforming any Markdown backtick code
spans (beginning and ending with a single backtick) into HTML code elements.</p>
</dd>
<dt><a href="#redden">redden(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as red colored if ANSI escapes are supported.</p>
</dd>
<dt><a href="#underline">underline(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as underlined if ANSI escapes are supported.</p>
</dd>
<dt><a href="#yellow">yellow(text)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the supplied string as yellow colored if ANSI escapes are supported.</p>
</dd>
</dl>

<a name="UnicodeEscapes"></a>

#### UnicodeEscapes : <code>enum</code>
**Kind**: global enum  
**Properties**

| Name | Type | Default |
| --- | --- | --- |
| infoSymbol | <code>string</code> | <code>&quot;ⓘ&quot;</code> | 
| midlineEllipsis | <code>string</code> | <code>&quot;⋯&quot;</code> | 
| ellipsis | <code>string</code> | <code>&quot;…&quot;</code> | 
| errorSymbol | <code>string</code> | <code>&quot;ⓧ&quot;</code> | 
| leftDoubleQuotes | <code>string</code> | <code>&quot;“&quot;</code> | 
| rightDoubleQuotes | <code>string</code> | <code>&quot;”&quot;</code> | 
| warningSymbol | <code>string</code> | <code>&quot;⚠&quot;</code> | 

<a name="blueify"></a>

#### blueify(text) ⇒ <code>string</code>
Returns the supplied string as blue colored if ANSI escapes are supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="curlyQuote"></a>

#### curlyQuote(text) ⇒ <code>string</code>
Returns the supplied string as curly quoted if Unicode is supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="ellipsify"></a>

#### ellipsify(text) ⇒ <code>string</code>
Returns the supplied string as ellipsified if Unicode is supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="italicize"></a>

#### italicize(text) ⇒ <code>string</code>
Returns the supplied string as italicized if ANSI escapes are supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="mdCodeSpans2html"></a>

#### mdCodeSpans2html(text) ⇒ <code>string</code>

<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OpenINF/GitHub-Markdown/HEAD/blockquotes/badge/light-theme/tip.svg">
  <img alt="Tip" src="https://raw.githubusercontent.com/OpenINF/GitHub-Markdown/HEAD/blockquotes/badge/dark-theme/tip.svg">
</picture><br />

This API will be deprecated in the next release in favor of one that follows
[Web Platform Design Principles](https://github.com/OpenINF/openinf-util-text/issues/169).

Processes the supplied string by transforming any Markdown backtick code spans
(beginning and ending with a single backtick) into HTML code elements.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="redden"></a>

#### redden(text) ⇒ <code>string</code>
Returns the supplied string as red colored if ANSI escapes are supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="underline"></a>

#### underline(text) ⇒ <code>string</code>
Returns the supplied string as underlined if ANSI escapes are supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<a name="yellow"></a>

#### yellow(text) ⇒ <code>string</code>
Returns the supplied string as yellow colored if ANSI escapes are supported.

**Kind**: global function  

| Param | Type |
| --- | --- |
| text | <code>string</code> | 

<br /><br />

---

<br />

### Contributing

Pull requests are welcome. For major changes, please open an issue first to
discuss what you would like to change. If for whatever reason you spot something
to fix but cannot patch it yourself, please [open an issue][].

<br />

### License

This project is licensed under either of

- [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
- [MIT license](https://opensource.org/licenses/MIT)

at your option.

The [SPDX](https://spdx.dev) license identifier for this project is
`MIT OR Apache-2.0`.

<br /><br />

---

<br />

<div align="center">

### Show Your Support

<br />

If you like the project (or want to bookmark it)&nbsp;&mdash;<br />
&mdash;&nbsp;[give it a star ⭐️][]&nbsp;&mdash;&nbsp;it will greatly encourage
us.

<br /><br />

<a title="The OpenINF website" href="https://open.inf.is" rel="author">
  <img alt="The OpenINF logo" height="32px" width="32px" src="https://raw.githubusercontent.com/openinf/openinf.github.io/live/assets/img/svg/logo.svg?sanitize=true" />
</a>

</div>

<br /><br />

[![Orange banner indicating a preview software component][release-level-banner--unstable]](##)

<!-- BEGIN LINK DEFINITIONS -->
[AI Risk Management Framework]:
  https://www.deepmind.com/publications/ethical-and-social-risks-of-harm-from-language-models
[conventional-commits-badge]: https://img.shields.io/badge/commit%20style-Conventional-%23fa6673?logoColor=white&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAzMCAzMCI+PHBhdGggc3R5bGU9ImZpbGw6ICNGRkYiIGQ9Ik0xNSwyQTEzLDEzLDAsMSwxLDIsMTUsMTMsMTMsMCwwLDEsMTUsMm0wLTJBMTUsMTUsMCwxLDAsMzAsMTUsMTUsMTUsMCwwLDAsMTUsMFoiLz48L3N2Zz4K 'Commit Style: Conventional Commits'
[conventional-commits-url]: https://www.conventionalcommits.org 'Commit Style: Conventional Commits'
[ethical and social risks of harm from LMs]:
  https://www.nist.gov/itl/ai-risk-management-framework
[give it a star ⭐️]: https://github.com/OpenINF/openinf-util-text/stargazers
[license-badge--shields]: https://img.shields.io/badge/license-MIT%2FApache--2.0-blue.svg?logo=github 'License: MIT/Apache 2.0'
[license-badge-url]: #license 'License: MIT/Apache 2.0'
[matrix-badge--shields]: https://img.shields.io/badge/matrix-join%20chat-%2346BC99?logo=matrix 'Chat on Matrix'
[matrix-url]: https://matrix.to/#/#openinf-space:matrix.org 'You&apos;re invited to talk on Matrix'
[npm-badge--shields]: https://img.shields.io/npm/v/@openinf/util-text/latest.svg?logo=npm&color=fe7d37 'View on npm'
[npm-badge-url]: https://www.npmjs.com/package/@openinf/util-text#top 'View on npm'
[open an issue]: https://github.com/OpenINF/openinf-util-text/issues
[prettier-badge]: https://img.shields.io/badge/code_style-Prettier-ff69b4.svg?logo=prettier 'Code Style: Prettier'
[prettier-url]: https://prettier.io/playground 'Code Style: Prettier'
[project-status-badge]: https://img.shields.io/badge/project%20status-under%20construction-orange 'Project Status: Under construction badge'
[release-level-banner--unstable]: https://raw.githubusercontent.com/OpenINF/openinf.github.io/live/assets/img/svg/release-level-banner--unstable.svg?sanitize=true 'Banner for Release Level: Unstable'
<!-- END LINK DEFINITIONS -->
