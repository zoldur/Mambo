# MamboCoin
Shell script to install a [MamboCoin Masternode](http://mambocoin.com) on a Linux server running Ubuntu 16.04. Use it on your own risk.  

***
## Installation:  

wget -q https://raw.githubusercontent.com/zoldur/MamboCoin/master/mambocoin.sh  
bash mambocoin.sh
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the MamboCoin Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **30000** MAMBO to **MN1**.  
4. Wait for 20 confirmations.  
5. Go to **Help -> "Debug Windwow - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **MamboNodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**  

***

## Usage:  

For security reasons **MamboCoin** is installed under **mambocoin** user, hence you need to **su - mambocoin** before checking:    

```
su - mambocoin
mambocoind masternode status
mambocoind getinfo
```  
Also, if you want to check/start/stop **mambocoind** , run one of the following commands as **root**:
```
systemctl status mambocoind #To check the service is running  
systemctl start mambocoind #To start mambocoind service  
systemctl stop mambocoind #To stop cropcpoind service  
```


***

  
Any donation is highly appreciated  

**MAMBO**: mSdfTLoh1R8P9UCGfGB1WWMCBrMg5any6k   
**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  

