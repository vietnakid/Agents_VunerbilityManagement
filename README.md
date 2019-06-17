# Agents_VunerbilityManagement
Agents_VunerbilityManagement

## Install
### Install requirement tools
* Agent machine need to install: nmap, xinetd and python3
```
sudo apt-get update
sudo apt-get install nmap xinetd python3 -y
```

* Create folder to store log file:
```
mkdir -p /var/log/nmap
mkdir -p /var/log/nse
```

### Deploy Agent

* For Nmap Agent:
	* Install nmap, xinetd
	* Change directory to `nmapAgent` and run `python3 deploy.py`

* For NSE Agent:
	* Install nmap, xinetd
	* Change directory to `nseAgent` and run `python3 deploy.py`

* For Wappalyzer Agent:
	* Install nodejs and npm first (Google scan for this step)
	* Use npm to install wappalyzer package in `https://www.npmjs.com/package/wappalyzer` by this command `npm i -g wappalyzer`
	* Change directory to `wappalyzerAgent` and run `python3 deploy.py`

* For CVE-Search Agent:
	* Install xinetd
	* If you not using docker, you have to re-configure in the deploy.py file. We recommend to use docker at here: https://hub.docker.com/r/ttimasdf/cve-search/
	* Change directory to `cveSearchAgent` and run `python3 deploy.py`