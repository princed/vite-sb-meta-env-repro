# Vite storybook meta env reproduction

Reproduction for <PR link>

## Instructions

1. After checkout run `yarn`
2. Run `yarn build-storybook` and notice it breaking with following message:
<details>

```
$ build-storybook
info @storybook/react v6.5.9
info 
info => Cleaning outputDir: /<repo-root>/storybook-static
info => Loading presets
info => Compiling manager..
vite v2.9.12 building for production...
✓ 275 modules transformed.
[rollup-plugin-dynamic-import-variables] Unexpected token (13:42)
file: /<repo-root>/src/App.tsx:13:42
transforming (1567) node_modules/hastscript/factory.jsinfo => Manager built (9.25 s)
ERR! SyntaxError: Unexpected token (13:42)
ERR!     at Parser.pp$4.raise (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19738:13)
ERR!     at Parser.pp$9.unexpected (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17032:8)
ERR!     at Parser.pp$9.semicolon (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17009:66)
ERR!     at Parser.pp$8.parseExpressionStatement (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17492:8)
ERR!     at Parser.pp$8.parseStatement (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17225:24)
ERR!     at Parser.pp$8.parseBlock (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17508:21)
ERR!     at Parser.pp$5.parseFunctionBody (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19564:22)
ERR!     at Parser.pp$5.parseArrowExpression (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19525:8)
ERR!     at Parser.pp$5.parseParenArrowList (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19254:15)
ERR!     at Parser.pp$5.parseParenAndDistinguishExpression (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19220:19)
ERR!     at Parser.pp$5.parseExprAtom (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19072:41)
ERR!     at Parser.pp$5.parseExprSubscripts (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18905:19)
ERR!     at Parser.pp$5.parseMaybeUnary (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18871:17)
ERR!     at Parser.pp$5.parseExprOps (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18798:19)
ERR!     at Parser.pp$5.parseMaybeConditional (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18781:19)
ERR!     at Parser.pp$5.parseMaybeAssign (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18748:19)
ERR!  SyntaxError: Unexpected token (13:42)
ERR!     at Parser.pp$4.raise (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19738:13)
ERR!     at Parser.pp$9.unexpected (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17032:8)
ERR!     at Parser.pp$9.semicolon (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17009:66)
ERR!     at Parser.pp$8.parseExpressionStatement (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17492:8)
ERR!     at Parser.pp$8.parseStatement (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17225:24)
ERR!     at Parser.pp$8.parseBlock (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:17508:21)
ERR!     at Parser.pp$5.parseFunctionBody (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19564:22)
ERR!     at Parser.pp$5.parseArrowExpression (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19525:8)
ERR!     at Parser.pp$5.parseParenArrowList (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19254:15)
ERR!     at Parser.pp$5.parseParenAndDistinguishExpression (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19220:19)
ERR!     at Parser.pp$5.parseExprAtom (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:19072:41)
ERR!     at Parser.pp$5.parseExprSubscripts (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18905:19)
ERR!     at Parser.pp$5.parseMaybeUnary (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18871:17)
ERR!     at Parser.pp$5.parseExprOps (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18798:19)
ERR!     at Parser.pp$5.parseMaybeConditional (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18781:19)
ERR!     at Parser.pp$5.parseMaybeAssign (/<repo-root>/node_modules/rollup/dist/shared/rollup.js:18748:19) {
ERR!   pos: 420,
ERR!   loc: Position { line: 13, column: 42 },
ERR!   raisedAt: 421,
ERR!   code: 'PLUGIN_ERROR',
ERR!   plugin: 'rollup-plugin-dynamic-import-variables',
ERR!   hook: 'transform',
ERR!   id: '/<repo-root>/src/App.tsx',
ERR!   watchFiles: [
ERR!     '/<repo-root>/iframe.html',
ERR!     '/virtual:/@storybook/builder-vite/vite-app.js',
ERR!     'vite/modulepreload-polyfill',
ERR!     '/<repo-root>/node_modules/vite/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/preview-web/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/client-api/package.json',
ERR!     '/virtual:/@storybook/builder-vite/setup-addons.js',
ERR!     '/virtual:/@storybook/builder-vite/storybook-stories.js',
ERR!     '/<repo-root>/node_modules/@storybook/preview-web/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/client-api/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/react/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-links/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-docs/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-actions/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-backgrounds/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-measure/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-outline/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addon-interactions/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/react/dist/esm/client/docs/config.js',
ERR!     '/<repo-root>/node_modules/@storybook/react/dist/esm/client/preview/config.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-links/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-docs/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-actions/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-backgrounds/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-measure/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-outline/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-interactions/preview.js',
ERR!     '/<repo-root>/.storybook/preview.js',
ERR!     'vite/preload-helper',
ERR!     '/<repo-root>/node_modules/@storybook/channel-postmessage/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/channel-websocket/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/addons/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/channel-postmessage/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/channel-websocket/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/addons/dist/esm/public_api.js',
ERR!     '/<repo-root>/node_modules/@storybook/store/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/store/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/preview-web/dist/esm/Preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/preview-web/dist/esm/PreviewWeb.js',
ERR!     '/<repo-root>/node_modules/@storybook/preview-web/dist/esm/simulate-pageload.js',
ERR!     '/<repo-root>/node_modules/@storybook/preview-web/dist/esm/types.js',
ERR!     '/<repo-root>/node_modules/@storybook/docs-tools/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/docs-tools/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/react/dist/esm/client/docs/extractArgTypes.js',
ERR!     '/<repo-root>/node_modules/@storybook/react/dist/esm/client/docs/jsxDecorator.js',
ERR!     '/<repo-root>/node_modules/@storybook/react/dist/esm/client/preview/render.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-links/dist/esm/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-actions/dist/esm/preset/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/client-api/dist/esm/ClientApi.js',
ERR!     '/<repo-root>/node_modules/@storybook/client-api/dist/esm/types.js',
ERR!     '/<repo-root>/node_modules/@storybook/client-api/dist/esm/queryparams.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-docs/dist/esm/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-measure/dist/esm/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-backgrounds/dist/esm/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-interactions/dist/esm/preset/preview.js',
ERR!     '/<repo-root>/node_modules/@storybook/addon-outline/dist/esm/preset/preview.js',
ERR!     '/<repo-root>/node_modules/core-js/package.json',
ERR!     '/<repo-root>/node_modules/global/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/channels/package.json',
ERR!     '/<repo-root>/node_modules/@storybook/client-logger/package.json',
ERR!     '/<repo-root>/node_modules/telejson/package.json',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.object.to-string.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/web.dom-collections.for-each.js',
ERR!     '/<repo-root>/node_modules/global/window.js',
ERR!     '/<repo-root>/node_modules/@storybook/channels/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/client-logger/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/telejson/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/core-events/package.json',
ERR!     '/<repo-root>/node_modules/qs/package.json',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.iterator.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.object.from-entries.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.filter.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.object.entries.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.object.assign.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.number.is-integer.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.number.constructor.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.regexp.exec.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.string.search.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.promise.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.map.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.includes.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.string.includes.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.object.values.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.concat.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.string.iterator.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/web.dom-collections.iterator.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/web.url.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/web.url-search-params.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.slice.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.symbol.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.symbol.description.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.symbol.iterator.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.function.name.js',
ERR!     '/<repo-root>/node_modules/core-js/modules/es.array.from.js',
ERR!     '/<repo-root>/node_modules/@storybook/core-events/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/qs/lib/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/addons/dist/esm/index.js',
ERR!     '/<repo-root>/node_modules/@storybook/addons/dist/esm/make-decorator.js',
ERR!     '/<repo-root>/node_modules/@storybook/addons/dist/esm/types.js',
ERR!     '/<repo-root>/node_modules/@storybook/addons/dist/esm/storybook-channel-mock.js',
ERR!     ... 337 more items
ERR!   ]
ERR! }
info => Loading presets
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.

Process finished with exit code 1

```
</details>

 3. Compare to running both `yarn storybook` and `yarn build` which both run just fine.
