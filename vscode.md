# Visual Studio code
This stuff gets lost all the time.. 

Packages: 
- `go`, [lukehoban](https://marketplace.visualstudio.com/items?itemName=lukehoban.Go)
- `Markdown All In One`, [yzhang](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- `Atom bindings`, [MS-Vscode](https://marketplace.visualstudio.com/items?itemName=ms-vscode.atom-keybindings)
- `Pythob`, [MS-Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

```json
{
    "go.lintTool": "gometalinter",
    "go.lintFlags": [
        "--disable-all",
        "--enable=vet",
        "--enable=vetshadow",
        "--disable=gotype",
        "--enable=golint",
        "--enable=ineffassign",
        "--enable=gas"
    ],
    "atomKeymap.promptV3Features": true,
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.formatOnPaste": true,
    "[markdown]": {
        "editor.wordWrap":"off"
    },
}
```
