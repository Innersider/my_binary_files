**How to run UDPSpeeder inside Android Termux:**

1. uninstall termux from Play Store, since it's no longer maintained anymore;

2. install Termux from Official Git Repo.

3. ```pkg update```

4. ```pkg install wget```

5. ```wget https://raw.githubusercontent.com/Innersider/my_binary_files/main/udpspeeder```

6. ```chmod +x udpspeeder```

7. ```./udpspeeder -c -l127.0.0.1:3331 -r<VPS-IP>:8448 -k "udpspeeder password"  -f10:6 --timeout 3 --mode 0 -i 10```

8. Clash for Android -> settings -> network -> set ACLS as not allowing the selected app, then select nekobox and termux

9. configure the ipcidr rules of VPS-IP in clash rules: field:

```- IP-CIDR,{$VPS-IP}/32,DIRECT,no-resolve```

10. configure nekobox as mode socks proxy only, and listening port as the same as the local socks5 proxy port in Clash config .

11. Keep termux running, keep nekobox running, now enable Clash for Android VPNService, All done.
