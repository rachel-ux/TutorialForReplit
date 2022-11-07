MediBlock- A ONE-STOP DESTINATION FOR INTEROPERABILITY BETWEEN PATIENTS AND DOCTORS
"MediBlock" is an online portal that maintains a digital copy of a patient’s medical history, along with all of their diagnosis and prescriptions.

Installation
The projects requires NodeJS and npm to work. Instructions to install all other dependencies are given below.

Node modules
1. Move to the project directory and open it in your terminal.
2. Run npm install to install project dependenccties.

IPFS
1. Go to the github page of IPFS and install IPFS Desktop

Local server
1. Install Node lite-server by running the following command on your terminal npm install -g lite-server

Metamask
1. Metamask is a browser extension available for Google Chrome, Mozilla Firefox and Brave Browser.
2. Go to the this link and add Metamask to your browser.

Getting the dApp running

Configuration

1. IPFS
Fire up your terminal and run ipfs init

Then run

ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin "['*']"
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials "['true']"
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods "['PUT', 'POST', 'GET']"
Note: If you face any issues with the above command on windows, try using command prompt and escape sequences or git bash.

2. Metamask
After installing Metamask, click on the metamask icon on your browser.
Click on TRY IT NOW, if there is an announcement saying a new version of Metamask is available.
Click on continue and accept all the terms and conditions after reading them.
Stop when Metamask asks you to create a new password. We will come back to this after deploying the contract in the next section.

Smart Contract

Install Truffle using npm install truffle -g
Compile Contracts using truffle compile

1. Starting your local development blockchain

Open Ganache.
Make sure to configure it the way mentioned above.
Open new Terminal and deploy contracts using truffle migrate
Copy deployed contract address to src/app.js
// app/src/app.js  line number 11
var agentContractAddress = '0x75E115394aacC7c6063E593B9292CB9417E4cbeC';
If you change contents of any contract , replace existing deployment using truffle migrate --reset
Note : reset of the contract will change the contract Address which needs to be updated in src/app.js

Running the dApp

1. Connecting Metamask to our local blockchain
Connect metamask to localhost:8485
Click on import account
Select any account from ganache and copy the private key to import account into metaMask

2. Starting IPFS
Start the IPFS Desktop Application

3. Start a local server
Open a new terminal window and navigate to /YOUR_PROJECT_DIRECTORY/app/.
Run npm start.
Open localhost:3000 on your browser.
That's it! The dApp is up and running locally.


