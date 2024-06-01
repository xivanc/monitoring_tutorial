# RPC monitoring tutorial
This is a simple demonstration of how to use our [RPC monitoring tool](https://www.noderpc.xyz/rpc_monitoring) to effectively monitor the health of any EVM RPC endpoint (such as Ethereum, Polygon, etc). For this demonstration, we've copied a simple NextJS [blog](https://github.com/vercel/next.js/tree/canary/examples/blog) web application that will collect your RPC monitoring data every time it's visited.

Please follow these steps:
1) Go to [RPC monitoring tool](https://www.noderpc.xyz/rpc_monitoring) and connect your wallet
2) Click the `Create monitoring` button and create a new RPC monitoring entity
3) Copy and paste the NextJS script generated at the bottom of the web page
4) In the copy-pasted script replace `const RPC_URL = "YOUR_RPC_PROVIDER_URL_HERE"` with the URL of the RPC endpoint you want to monitor. If you don't have an endpoint, you can use our Ethereum mainnet test endpoint for this demonstration. For example, the updated line can look like this ```const RPC_URL = "https://api.noderpc.xyz/rpc-mainnet/2ab6fa32d9c7d78cc06ca652490"```
5) Clone this github repo into your local folder: `git clone git@github.com:xivanc/monitoring_tutorial.git`
6) In your local folder, in the `pages/_app.tsx` file, paste your modified script anywhere inside the `<Head>` tag
7) Install the dependencies and run the web page locally: ```yarn install; yarn dev -p 3000```
8) Refresh your localhost page `http://localhost:3000/` once a minute. Do this several times to simulate some traffic so that some monitoring data can be collected
9) Go back to the [monitoring tool](https://www.noderpc.xyz/rpc_monitoring) where you should be able to see some health statistics of your EVM RPC endpoint
