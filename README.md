# Whatsales
Guide to reconnect a Whatsapp Line via AWS ssh console.
### Downloading 
First you must download the ZIP file containing the celina_key.pem file. Click on the "<> code" button and then download ZIP. And finally, extract the file to a folder.
### Execution
Open a CMD terminal in the folder where we extracted the file and execute:
```bash
ssh -i "celina_key.pem" ubuntu@ec2-34-239-42-108.compute-1.amazonaws.com
```
Type "Y" if applicable.
Move to the folder database-celina:
```bash
cd database-celina/
```
Remove creds from disconnected line:
```bash
rm -rf auth_info_baileys/
```
Restart the pm2 0:
```bash
pm2 restart 0 
```
Open the logs to see the QR and scan:
```bash
pm2 logs 0 
```


