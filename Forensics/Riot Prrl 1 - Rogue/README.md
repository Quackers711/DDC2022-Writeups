# Riot Prrl 1 - Rouge
### Description
>Du er blevet indkaldt til en tophemmelig mission af Interpoliti.  
Læs briefing.pdf for mere info.  
Astrid Mågensdals computer er filen r0uge3fa1ry.ova.
>
>OBS: Det kan tage lidt tid at downloade Astrids computer. Måske er der andet information du kan finde om hende imens?

## Løsning
Eftersom at `.ova` filen fylder omkring 2GB har vi lidt tid til at lave noget research på Astrid som desdeskriptionen også forslår. I briefing filen får vi at vide at hun bruger navnet `astridmagensdal` online.

Lad os slippe for at skulle gøre det hårde arbejde og bare smide navnet ind i toolet ![Sherlock](https://github.com/sherlock-project/sherlock)

>[*] Checking username astridmagensdal on:
>
>[+] Coil: https://coil.com/u/astridmagensdal
>
>[+] Fiverr: https://www.fiverr.com/astridmagensdal
>
>[+] Instagram: https://www.instagram.com/astridmagensdal
>
>[+] Minecraft: https://api.mojang.com/users/profiles/minecraft/astridmagensdal
>
>[+] TradingView: https://www.tradingview.com/u/astridmagensdal/
>
>[+] Twitter: https://twitter.com/astridmagensdal

Mange af resultaterne er døde links eller irrelevante men Instagram og Twitter stikker ud som værende de mest interessante i dette tilfælde.

Ved at kigge på hendes Instagram finder vi en mistænkelig post: https://www.instagram.com/p/CcBJiZjrMo8/
Noget der ligner et password på en notesblok!

Vi kan nu starte hendes maskine op i VMware og logge ind.
Min første ide var  at prøve usernamet `root` og passwordet `QqgepcyRf9Aa` fra Instagram posten og det virkede. Vi har nu adgang til hendes maskine!

Eftersom at vi er logget ind med root ligger der ikke nogle speciale filer i vores directory denne gang. Men hvis vi skifter til `/home/astrid/` finder vi alle hendes personlige filer og det første flag i filen `flag.txt`!

>DDC{I_w0nd3R_1f_AsTr1d_haS_a_h1st0Ry_w1Th_a_s3Rv3r}
