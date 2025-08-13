# Patching the vulnerabilities:
To patch CWE 548, I made an .htaccess file under the directory of DVWA in VSCode. The .htaccess file is a configuration file that manages how the server would respond to requests. 
In this case, the file controls the access of the directory and the files under it. Whenever a user attempts to check the directory folders, the server should only display an error message.
<img width="1078" height="416" alt="CWE-548_patching" src="https://github.com/user-attachments/assets/5758580e-18c5-424a-9441-1e556a97fc73" />
##
To patch CWE 597, I needed access to the Apache main configuration folder. I did that using this command:
<img width="1017" height="202" alt="CWE-497_patching1" src="https://github.com/user-attachments/assets/12f9952c-0a33-4c86-b66d-d149620b9313" />
Afterwards, I opened the apache2.conf file which is the main configuration file of Apache. I placed two commands, “ServerTokens Prod” which tells the server not to send any versions in the HTTP header and “ServerSignature Off” to hide the server version in the error messages. 
After patching the vulnerabilities, I saved the changes and restarted the server for the changes to take effect.
##
When I try to access the directories once again, I got an error message without further details:
<img width="862" height="377" alt="CWEs_patched1" src="https://github.com/user-attachments/assets/4ed0e296-9349-45e8-9eed-967cbd7692e9" />
<img width="800" height="347" alt="CWEs_patched2" src="https://github.com/user-attachments/assets/ba6e3ebe-d0c0-411e-931b-b6c3892d42ad" />
##
This means that the two vulnerabilities are now patched. Making the web application safe from exposed directories, folders and files as well as the version of the server managing it.

