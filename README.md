# forge-hubs-browser-dotnet

![platforms](https://img.shields.io/badge/platform-windows%20%7C%20osx%20%7C%20linux-lightgray.svg)
[![.net](https://img.shields.io/badge/net-6.0-blue.svg)](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
[![license](https://img.shields.io/:license-mit-green.svg)](https://opensource.org/licenses/MIT)

Simple [Autodesk Forge](https://forge.autodesk.com) application built by following
the [Hubs Browser](https://forge-tutorials.autodesk.io/tutorials/hubs-browser/) tutorial
from https://forge-tutorials.autodesk.io.

![screenshot](screenshot.png)

## Development

### Prerequisites

- [Forge application](https://forge.autodesk.com/en/docs/oauth/v2/tutorials/create-app)
- Provisioned access to [BIM 360 Docs](https://forge.autodesk.com/en/docs/bim360/v1/tutorials/getting-started/manage-access-to-docs/)
or Autodesk Construction Cloud
- [.NET 6](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- Terminal (for example, [Windows Command Prompt](https://en.wikipedia.org/wiki/Cmd.exe)
or [macOS Terminal](https://support.apple.com/guide/terminal/welcome/mac))

### Setup & Run

- Clone this repository
- Install dependencies: `yarn install` or `npm install`
- Setup environment variables:
  - `FORGE_CLIENT_ID` - your Forge application client ID
  - `FORGE_CLIENT_SECRET` - your Forge application client secret
  - `FORGE_CALLBACK_URL` - URL for your users to be redirected to after they successfully log in with their Autodesk account
    - For local development, the callback URL is `http://localhost:8080/api/auth/callback`
    - For applications deployed to a custom domain, the callback URL is `http://<your-domain>/api/auth/callback` or `https://<your-domain>/api/auth/callback`
    - Do not forget to update the callback URL for your application in https://forge.autodesk.com/myapps as well
  - `SERVER_SESSION_SECRET` - arbitrary phrase used to encrypt/decrypt server session cookies
- Run the server: `yarn start` or `npm start`

> When using [Visual Studio Code](https://code.visualstudio.com),
you can specify the env. variables listed above in a _.env_ file in this
folder, and run & debug the application directly from the editor.

## Troubleshooting

Please contact us via https://forge.autodesk.com/en/support/get-help.

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT).
Please see the [LICENSE](LICENSE) file for more details.
