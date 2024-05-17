# start

## home page
- route: /
- ```ts
    import { serveFile, serveDir } from "jsr:@std/http/file-server";
    input.response = serveFile(input.request, Deno.cwd()+'/static/index.html')
    ```

## serve assets
- route: /assets/*
- ```ts
    input.response = serveDir(input.request, {
        fsRoot: Deno.cwd()+'/static'
    })
    ```
