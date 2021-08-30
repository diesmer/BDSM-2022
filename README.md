# Diesmer Hensbergen - 1662367 - diesmer.hensbergen@student.hu.nl
# Letterfrequenties
# LanguageClassifier
De classifier maakt gebruik van een mapper & reducer, wat gemaakt is in Java voor gebruik met Hadoop
# Run
Uit de `build` folder is de `.JAR` file de nieuwste build. Deze moet je uitvoeren met hetvolgende commando:

`hadoop jar *PATH-TO-JAR*/LanguageClassifier-1.jar LanguageClassifier.WordCount.WordCount *PATH-TO-INPUT* *PATH-TO-OUTPUT*`

In de `testfiles` folder staan de gebruikte teksten.

Hetvolgende moet als output eruit komen:
- ![Alt text](screenshots/output.png?raw=true "Hadoop output")

Deze bestanden in de `output` folder geplaatst
- ![Alt text](screenshots/output_folder_content.png?raw=true "Folder content")
- De output van het programma staat in het `part-r-00000` bestand

De output van de nieuwste build is ook te vinden in de `latest_build_output` folder van deze repo in het bestand `output.txt`
# JAR genereren
Om zelf een `.JAR` te genereren, gebruik het commando `maven install` vanuit _Eclipse_ of _IntelliJ_

De `.JAR` die hier gebruikt wordt is gegenereerd met _Eclipse_
# Testfiles
`test.txt` --> testbestand waar een mix van nederlandse en engelse zinnen in staan
`test.sh` --> BASH-script die gebruikt is voor het testen
`dutch.txt` --> NRC artikelen uit 2012
`english.txt` --> de engelstalige versie van Alice in Wonderland

# Precision
De resultaten van de classifier zijn niet fijloos; hij maakt zo hier en daar nog een fout waar hij nederlands voor engels aan ziet en vice versa. 

- 193 regels in totaal
- 74 Nederlandse regels
- 117 Engelse regels

Daarmee kun je berekenen:
- `93,25%` correct - Nederlands
- `95,79%` correct - Engels
- ![Alt text](screenshots/output_last_lines.png?raw=true "Last lines from output file")