# Monetization with Salable Miro App

This app shows how to use Salable to create Miro apps with advanced licensing and monetization features.

# 👨🏻‍💻 App Demo

https://github.com/user-attachments/assets/c6111206-e294-4dfb-a26c-59b2e2395204

# 📒 Table of Contents

- [Included Features](#features)
- [Tools and Technologies](#tools)
- [Prerequisites](#prerequisites)
- [Salable Prerequisites](#salableprerequisites)
- [Run the app locally](#run)

# ⚙️ Included Features <a name="features"></a>

- [Miro Web SDK](https://developers.miro.com/docs/web-sdk-reference)
  - [on(icon:click)](https://developers.miro.com/docs/ui_boardui#iconclick-event)
  - [openPanel(options)](https://developers.miro.com/docs/ui_boardui#openpanel)

# 🛠️ Tools and Technologies <a name="tools"></a>

- [React](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Next.js](https://nextjs.org/)
- [Salable](https://docs.salable.app/docs/quick-start-guide)

# ✅ Prerequisites <a name="prerequisites"></a>

- You have a [Miro account](https://miro.com/signup/).
- You're [signed in to Miro](https://miro.com/login/).
- Your Miro account has a [Developer team](https://developers.miro.com/docs/create-a-developer-team).
- <b>You have a [Salable account](https://salable.app/signup)</b>
- Your development environment includes [Node.js 14.13](https://nodejs.org/en/download) or a later version.
- All examples use `npm` as a package manager and `npx` as a package runner.

# 📖 Associated Developer Tutorial <a name="tutorial"></a>

> To view a more in depth developer tutorial
> of this app (including code explanations) see the [Monetization with Miro and Salable tutorial](https://developers.miro.com/docs/monetization-with-miro-salable) on Miro's Developer documentation.

# ✅ Salable Prerequisites <a name="stripeprerequisites"></a>

1. [Create an account](https://salable.app/signup) on Salable
2. Create an [API Key in Salable](https://salable.app/settings/api-keys?modal=add-api-key)
3. Set up a [payment integration](https://docs.salable.app/docs/using-the-dashboard/payment-integration/add-salable-payments) in Salable (such as Stripe)
4. Configure a _product_ and _plan_ in Salable. See the complete step-by-step process in our guide [here](https://developers.miro.com/docs/monetization-with-miro-salable).

# 🏃🏽‍♂️ Run the app locally <a name="run"></a>

1. Rename the ['.env.example' file](.env.example) to `.env` and then add your credentials for both platforms. You will need to create a Miro app and then add in the access token along with Salable API key, product ID, and plan ID.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start developing. \
   Your URL should be similar to this example:
   ```
   http://localhost:3000
   ```
4. Open the [app manifest editor](https://developers.miro.com/docs/manually-create-an-app#step-2-configure-your-app-in-miro) by clicking **Edit in Manifest**. \

   In the app manifest editor, configure the app as follows and click save:

```yaml
# See https://developers.miro.com/docs/app-manifest on how to use this
appName: Monetization with Salable
sdkVersion: SDK_V2
sdkUri: http://localhost:3000
redirectUris: http://localhost:3000/api/redirect/
scopes:
  - boards:read
  - boards:write
```

5. Go to **Redirect URI for OAuth2.0**, click **Options**. for the localhost path. \
   From the drop-down menu select **Use this URI for SDK authorization**.

6. Go back to your app home page, and under the `Permissions` section, you will see a blue button that says `Install app and get OAuth token`. Click that button. Then click on `Add` as shown in the video below.

> ⚠️ We recommend to install your app on a [developer team](https://developers.miro.com/docs/create-a-developer-team) while you are developing or testing apps.⚠️

https://github.com/miroapp/app-examples/assets/10428517/1e6862de-8617-46ef-b265-97ff1cbfe8bf

7. Go to your developer team, and open your boards.
8. Click on the plus icon from the bottom section of your left sidebar. If you hover over it, it will say `More apps`.
9. Search for your app `Monetization with Salable` or whatever you chose to name it. Click on your app to use it, as shown in the video below.

https://github.com/horeaporutiu/app-examples-template/assets/10428517/b23d9c4c-e785-43f9-a72e-fa5d82c7b019
