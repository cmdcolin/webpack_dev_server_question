# webpack_dev_server_question

When I use this app under webpack_dev_server and with an `npm linked` module it causes the app to fail



## Setup

    git clone git@github.com:cmdcolin/webpack_dev_server_question
    cd webpack_dev_server_question
    yarn

Then clone bbi-js

    git clone git@github.com:gmod/bbi-js
    cd bbi-js
    yarn
    yarn build
    yarn link


Then cd back to webpack_dev_server_question

    yarn link @gmod/bbi
    npx webpack-dev-server


Then cd back to bbi-js

    yarn build


This causes the webpack-dev-server to fail with the file not found error on @gmod/bbiA


## Error

```
ERROR in ../src/gmod/bbi-js/dist/index.js
Module build failed: Error: ENOENT: no such file or directory, open '/home/cdiesh/src/gmod/bbi-js/dist/index.js'
 @ ./src/index.js 1:0-32
 @ multi (webpack)-dev-server/client?http://localhost:8080 ./src
ℹ ｢wdm｣: Failed to compile.

```


## Env

Node v10.15.0
webpack-dev-server 3.1.14
webpack 4.29.0

