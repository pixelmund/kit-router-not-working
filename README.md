# Router not working in production

Steps to reproduce:

-  pnpm install
-  pnpm build 
-  pnpm start
-  Click on the doesn't work button and view error logs

It seems to me that upon reaching a reasonable size the singletons module gets included inside vendor.js and so the router is set before the init function is invoked, maybe the singletons should always be its own module or refactor into a class? 