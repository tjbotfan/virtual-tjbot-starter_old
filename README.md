Virtual TJBot Starter Application
====================================

### Node-RED and Virtual TJBot on IBM Cloud

このレポジトリはVirtual TJBotを利用するために必要なNode-REDのアプリケーションと設定・フローデータをIBMCloud のアプリケーションとして設定するためのツール集です。
`Deploy to IBM Cloud` ボタンをクリックすると専用の環境が作成されます。

※利用にはIBM Cloudのライトアカウント以上の登録が必要になります。

[![Deploy to IBM Cloud](./button.png)](https://bluemix.net/deploy?repository=https://github.com/tjbotfan/virtual-tjbot-starter.git)

This repository is a collection of tools for configuring Node-RED applications and configuration / flow data necessary for using Virtual TJBot as IBM Cloud applications.
Click the `Deploy to IBM Cloud` button to create a dedicated environment.

* To use, you need to register at least as an IBM Cloud Lite account.

### Thanks

このプロジェクトは以下のプロジェクトに感謝します。
This project appreciate those projects:

- Node-RED
- Node-RED Starterkit
- IBM Open Toolchain
- node-red-contrib-virtual-tjbot



### How does this work?

When you click the button, you are taken to IBM Cloud where you get a pick a name
for your application at which point the platform takes over, grabs the code from
this repository and gets it deployed.

It will automatically create an instance of the Cloudant service and bind it to
your app. This is where your Node-RED instance will store its data.

When you first access the application, you'll be asked to set some security options
to ensure your flow editor remains secure from unauthorised access.

It includes a set of default flows that are automatically deployed the first time
Node-RED runs.

### Customising Node-RED

This repository is here to be cloned, modified and re-used to allow anyone create
their own Node-RED based application that can be quickly deployed to IBM Cloud.

The default flows are stored in the `defaults` directory in the file called `flow.json`.
When the application is first started, this flow is copied to the attached Cloudant
instance. When a change is deployed from the editor, the version in cloudant will
be updated - not this file.

The web content you get when you go to the application's URL is stored under the
`public` directory.

Additional nodes can be added to the `package.json` file and all other Node-RED
configuration settings can be set in `bluemix-settings.js`.

If you do clone this repository, make sure you update this `README.md` file to point
the `Deploy to IBM Cloud` button at your repository.

If you want to change the name of the Cloudant instance that gets created, the memory
allocated to the application or other deploy-time options, have a look in `manifest.yml`.
