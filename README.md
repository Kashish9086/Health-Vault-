# Health-Vault-Health Records Management Using Blockchain
Introduction
The aim of this framework is firstly to implement blockchain technology for EHR and secondly to provide secure storage of electronic records by defining granular access rules for the users of the proposed framework. Moreover, this framework also discusses the scalability problem faced by the blockchain technology in general via use of off-chain storage of the records. This framework provides the EHR system with the benefits of having a scalable, secure and integral blockchain-based solution.
Installation
The projects requires NodeJS and npm to work. Instructions to install all other dependencies are given below.

Node modules
Move to the project directory and open it in your terminal.
Run npm install to install project dependenccties.
Ganache
Go to Ganache homepage and download.
If you are on Linux, you must have received an .appimage file. Follow installation instructions available here.
IPFS
Go to the github page of IPFS and install IPFS Desktop
Local server
Install Node lite-server by running the following command on your terminal npm install -g lite-server
Metamask
Metamask is a browser extension available for Google Chrome, Mozilla Firefox and Brave Browser.
Go to the this link and add Metamask to your browser.
Getting the dApp running
Configuration
1. Ganache
Open Ganache and click on settings in the top right corner.
Under Server tab:
Set Hostname to 127.0.0.1 -lo
Set Port Number to 8545
Enable Automine
Under Accounts & Keys tab:
Enable Autogenerate HD Mnemonic
2. IPFS
Fire up your terminal and run ipfs init

Then run

ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin "['*']"
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials "['true']"
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods "['PUT', 'POST', 'GET']"
Note: If you face any issues with the above command on windows, try using command prompt and escape sequences or git bash.

3. Metamask
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
