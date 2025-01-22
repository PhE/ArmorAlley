# dev workflow


## src/js only

Auto build on `src/js` changes:

```shell
# once in a session
npx npm run serve
npx npm run watch
```

or 

```shell
# once in a session
npx http-server
npx nodemon --watch src/js/ --exec "npx gulp build"
```


## src only

If you only work on `/src` files:

```shell
# once in a session
npx http-server

# on each source change
npx gulp build
```


## full build


```shell
# once in a session
npx http-server

# on each source/asset change
npx gulp
```
