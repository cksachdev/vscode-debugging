# vscode-debugging
repo to show issue with debugging in vscode

My program contains only 2 lines of code:
```
const XLSX = require('xlsx');
console.log("imported xlsx" + XLSX);
```

When I try to debug this in vscode, I get the following error:
ReferenceError: Blob is not defined
Refer to screenshot below:  
![Preview](https://github.com/cksachdev/docs/blob/master/vscode-debugging.png
)

To ignore the files from node_modules, I have tried adding 
```
"skipFiles": [
        "${workspaceFolder}/node_modules/**/*.js",
        "${workspaceFolder}/lib/**/*.js",
        "<node_internals>/**/*.js"
      ],
```
in launch.json. After adding skipFiles, none of the breakpoints get triggered e.g. if I put a breakpoint on console log statement, debugger never stops. Is this a kn