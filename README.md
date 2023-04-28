
> **Note** This repo contains a bug reproduction for @databases/pg.
> 
> See: https://github.com/ForbesLindesay/atdatabases/issues/291

To reproduce the bug, run `npm run build`

Should yield output similar to this:

```shell
atdatabases-pg-esm-bug@1.0.0 build
npx rimraf dist types && tsc

src/index.ts:3:7 - error TS2349: This expression is not callable.
  Type 'typeof import("/Users/xyz/Projects/atdatabases-pg-esm-bug/node_modules/@databases/pg/lib/index")' has no call signatures.

3 await createConnectionPool()
        ~~~~~~~~~~~~~~~~~~~~
```
