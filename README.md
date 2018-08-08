# DividendCash
Shell script to install a [Dividend.Cash Masternode](https://dividend.cash/) on a Linux server running Ubuntu 14.04 or 16.04. Use it on your own risk.

***
## Installation:
```
git clone https://github.com/dividendcash/dividendcash.git
cd dividendcash
bash dvd.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the Dividend.Cash Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **1000** **Dividend.Cash** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  ** Tools -> "Open Masternode Configuration File"
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is unlocked.
12. Open **Debug Console** and type:
```
startmasternode alias false MN1
```
***

## Usage:
```
dividendcash-cli getinfo
dividendcash-cli mnsync status
dividendcash-cli masternode status
```

***
