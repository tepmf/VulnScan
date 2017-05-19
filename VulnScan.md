# VulnScan


##### Begin Scan NMAP

“nmap -sn -n -oX "c:\*" 192.*.*.*/*”

“-sn” -> Ping scan;
“-n” -> não resolver endereços;
“-oX” -> Output xml file;
“c:\*” -> ficheiro de destino;
“192.*.*.*/*” -> rede a scannar

Opcional -> “--host-timeout 15s”


##### End Scan NMAP

##### Begin Scan Meta

sudo mount -t cifs -o credentials=/batatas/.smbcredentials,iocharset=utf8,file_mode=0777,dir_mode=0777 //myshare/share /mnt/point --verbose

grep "ipv4" /mnt/feijao/NmapOutput.xml | awk -F "\"" '{print $2}' > /batatas/arroz/InputMeta001

spool /batatas/arroz/results/cenouras.txt
set timestampoutput true
use auxiliary/scanner/smb/smb_ms17_010_artesanal
set rhosts file://batatas/arroz/InputMeta001
set threads 48


grep "MS17-010" console.log >> result-rabanetes-VUL.log

##### End Scan Meta
