#  Carbonmark API Integration to SAP - Demo App

This app uses the RESTful ABAP programming model along with the PRVD stack and provide-abap to pioneer the practice of integrating blockchain-based carbon offsets to carbon emissions data in SAP S/4 HANA. 

Use this app to:
- generate mock carbon emissions on SFLIGHT data in a SAP development sandbox
- acquire carbon retirements on KlimaDAO (Polygon) via PRVD stack, Provide Payments fiat-crypto bridge
- generate carbon emissions and atomic offset zero knowledge proofs through PRVD Axiom (e.g. Baseline Protocol)

This app integrates the [ carbon retirement aggregator](https://docs.klimadao.finance/developers/contracts/retirement) from the [Polygon Matic](https://polygon.technology/) mainnet. Learn more about KlimaDAO and the digital carbon market [here](https://docs.klimadao.finance/)

This is repo is for the frontend only. See the ABAP backend component repo and [Provide ECO API documentation](https://docs.provide.services/payments/eco/api) for more information on how the SAP - Blockchain integration is achieved via provide-abap and PRVD stack.

You can run the app front end either as a Node.js app on SAP BTP or deployed to a SAP Fiori Launchpad.

## Basic Dependencies and Todos

On your SAP system you will need to
- install and configure [provide-abap](https://github.com/provideplatform/provide-abap). Clone the provide-abap repo through abapGit - use the [provide-abap enablement docs](https://docs.provide.services/provide-abap) for additional details.
- install and configure SAP backend ECO demo application abapGit repo

Other todos
- Configure the SFLIGHT carbon emissions and atomic offset zk-workflows in [Provide Shuttle](https://shuttle.provide.services) (Additional instructions forthcoming)
- Pre-pay USDC to Provide Payments for demo usage

## Application Details
|               |
| ------------- |
|**Generation Date and Time**<br>Tue Feb 28 2023 23:24:48 GMT-0500 (Eastern Standard Time)|
|**App Generator**<br>@sap/generator-fiori-elements|
|**App Generator Version**<br>1.5.4|
|**Generation Platform**<br>Visual Studio Code|
|**Floorplan Used**<br>Worklist|
|**Service Type**<br>SAP System (ABAP On Premise)|
|**Service URL**<br> {{yourFioriLaunchpadURL}}/sap/opu/odata/sap/ZUI_C_PRVD_ECO_DEMO_0902V2
|**Module Name**<br>sflight-atomic-offsets|
|**Application Title**<br>Provide ECO SFLIGHT Atomic Offsets|
|**Namespace**<br>|
|**UI5 Theme**<br>sap_fiori_3|
|**UI5 Version**<br>1.102.8|
|**Enable Code Assist Libraries**<br>True|
|**Add Eslint configuration**<br>False|
|**Main Entity**<br>FlightData|
|**Navigation Entity**<br>to_AtomicOffset|


### Starting the generated app

-   Upon cloning this repo, install dependencies

```
    npm install
```

-   This app has been generated using the SAP Fiori tools - App Generator, as part of the SAP Fiori tools suite.  In order to launch the generated app, simply run the following from the generated app root folder:

```
    npm start
```

#### Offline - not yet supported

- Offline mock data support will be added soon! In order to run the application with Mock Data, run the following from the generated app root folder:

```
    npm run start-mock
```

#### Local runtime Pre-requisites:

1. Active NodeJS LTS (Long Term Support) version and associated supported NPM version.  (See https://nodejs.org)
2. UI5 Tools CLI (See https://sap.github.io/ui5-tooling/v3/pages/CLI/)

#### Integration to your Fiori Launchpad system

Note the web dispatcher URL of your Fiori launchpad system (eg. yourFioriLaunchpadURL) and update it in the ui5.yaml and related files


