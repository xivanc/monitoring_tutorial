# RPC monitoring tutorial
This is a simple demonstration of how to use our [RPC monitoring tool](https://www.noderpc.xyz/rpc_monitoring) to effectively monitor the health of any EVM RPC endpoint (such as Ethereum, Polygon, etc).

Please follow these steps:
1) Go to [RPC monitoring tool](https://www.noderpc.xyz/rpc_monitoring) and connect your wallet
2) Click the `Create monitoring` button and create a new RPC monitoring entity
3) Copy and paste the NextJS script generated at the bottom of the web page
4) In the copy-pasted script replace `const RPC_URL = "YOUR_RPC_PROVIDER_URL_HERE"` with the URL of the RPC endpoint you want to monitor. If you don't have an endpoint at hand, feel free to use our Ethereum mainnet test endpoint for this demonstration: `https://api.noderpc.xyz/rpc-mainnet/2ab6fa32d9c7d78cc06ca652490`. For example, the line will look like this ```const RPC_URL = "https://api.noderpc.xyz/rpc-mainnet/2ab6fa32d9c7d78cc06ca652490"```
5) Clone this github repo into your local folder: `git clone git@github.com:xivanc/monitoring_tutorial.git`
6) In the `pages/_app.tsx` file, paste your modified script anywhere inside the `<Head>` tag
7) Install the dependencies and run the web page locally: ```yarn install; yarn dev -p 3000```
8) Refresh the page once a minute, do this several times
9) Go back to the [monitoring tool](https://www.noderpc.xyz/rpc_monitoring) and you should be able to see the health statistics of your EVM endpoint.
