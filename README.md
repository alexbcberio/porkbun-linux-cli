# Porkbun API bash client

> The client under development, more features will be added with the time.

Porkbun v3 API client in bash. The script needs the following packages to be installed in the system:

- curl: to perform the HTTPS requests.
- jq: to parse and beautify the JSON responses.

## Supported API endpoints

The following API endpoints are the ones that will be supported, the currently implemented ones are marked with a check:

- General
  - [x] [Authentication (Ping)](https://porkbun.com/api/json/v3/documentation#Authentication)
  - [x] [Authentication (Ping ipv4)](https://porkbun.com/api/json/v3/documentation#ipv4)
- Domain
  - [ ] [Domain Update Name Servers](https://porkbun.com/api/json/v3/documentation#Domain%20Update%20Name%20Servers)
  - [ ] [Domain Get Name Servers](https://porkbun.com/api/json/v3/documentation#Domain%20Get%20Name%20Servers)
  - [x] [Domain List All](https://porkbun.com/api/json/v3/documentation#Domain%20List%20All)
  - [ ] [Domain Add Url Forward](https://porkbun.com/api/json/v3/documentation#Domain%20Add%20URL%20Forward)
  - [ ] [Domain Get URL Forwarding](https://porkbun.com/api/json/v3/documentation#Domain%20Get%20URL%20Forwarding)
  - [ ] [Domain Delete Url Forward](https://porkbun.com/api/json/v3/documentation#Domain%20Delete%20URL%20Forward)
- DNS
  - [x] [DNS Create Record](https://porkbun.com/api/json/v3/documentation#DNS%20Create%20Record)
  - [x] [DNS Edit Record by Domain and ID](https://porkbun.com/api/json/v3/documentation#DNS%20Edit%20Record%20by%20Domain%20and%20ID)
  - [x] [DNS Edit Records by Domain, Subdomain and Type](https://porkbun.com/api/json/v3/documentation#DNS%20Edit%20Record%20by%20Domain,%20Subdomain%20and%20Type)
  - [x] [DNS Delete Record by Domain and ID](https://porkbun.com/api/json/v3/documentation#DNS%20Delete%20Record%20by%20Domain%20and%20ID)
  - [x] [DNS Delete Records by Domain, Subdomain and Type](https://porkbun.com/api/json/v3/documentation#DNS%20Delete%20Records%20by%20Domain,%20Subdomain%20and%20Type)
  - [x] [DNS Retrieve Records by Domain or ID](https://porkbun.com/api/json/v3/documentation#DNS%20Retrieve%20Records%20by%20Domain%20or%20ID)
  - [ ] [DNS Retrieve Records by Domain, Subdomain and Type](https://porkbun.com/api/json/v3/documentation#DNS%20Retrieve%20Records%20by%20Domain,%20Subdomain%20and%20Type)

## Usage

1. Create API keys for your account, on [Account > API Access](https://porkbun.com/account/api)
2. Enable "API Access" on the domains, press on "Details" and check the "API Access" settings on the desires domains.
3. Execute the script, it will prompt for your API credentials the first time you launch it. The configuration file is saved on the same location as is the script.

   > The generated file is in plain text, with 600 (rw-------) permission.

4. Run again the script, a help page will be shown when encountering invalid parameters. Such as

   ```
   Usage: ./porkbun-linux-cli <command>

   Commands:
     ping  Test communication with the API, also returns the IP address.
     ping-ipv4  Test communication with the API, also returns the IP address in IPv4 format.
     dns  Manage DNS records

   Version: v0.1.0
   ```
