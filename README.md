to reproduce the problem:

1. run `pnpm i`
2. an error will be thrown from `dist/cli/cli-utils.mjs`:

   ```
   node:internal/modules/esm/resolve:854
     throw new ERR_MODULE_NOT_FOUND(packageName, fileURLToPath(base), null);
           ^

   Error [ERR_MODULE_NOT_FOUND]: Cannot find package 'consola' imported from /path/to/project/node_modules/.pnpm/wxt@0.19.2_@types+node@22.0.0_rollup@4.19.1/node_modules/wxt/dist/cli/cli-utils.mjs
       at packageResolve (node:internal/modules/esm/resolve:854:9)
       at moduleResolve (node:internal/modules/esm/resolve:927:18)
       at defaultResolve (node:internal/modules/esm/resolve:1169:11)
       at ModuleLoader.defaultResolve (node:internal/modules/esm/loader:383:12)
       at ModuleLoader.resolve (node:internal/modules/esm/loader:352:25)
       at ModuleLoader.getModuleJob (node:internal/modules/esm/loader:227:38)
       at ModuleWrap.<anonymous> (node:internal/modules/esm/module_job:87:39)
       at link (node:internal/modules/esm/module_job:86:36) {
     code: 'ERR_MODULE_NOT_FOUND'
   }
   ```
