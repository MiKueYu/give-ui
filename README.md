## GIVE-UI

Simple UI for the `SPT GIVE` command.

![recording.gif](recording.gif)

### How it works

1. With the server and preferably with Tarkov running, open the app
2. Use the form to connect to the server and select your character
3. Select the item you want to receive. The quantity is always set to the maximum stack size
4. You will receive a message with the item/s

### Development

```shell
TEMPL_EXPERIMENT=rawgo templ fmt components/templates.templ && TEMPL_EXPERIMENT=rawgo templ generate && wails dev -devserver 0.0.0.0:34115
```

### Release

- Update version in `wails.json`
- Update version in `server-mod/package.json`
- commit and push (TODO: automate this in future)
- Create a new release with proper tag
- Github action will take over and upload the zip
