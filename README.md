<img width="1213" height="572" alt="image" src="https://github.com/user-attachments/assets/03d673b5-a146-46c2-a214-f6041a5dba34" />

Skeem on ülal. Siin on olulisemad märkused ühenduste kohta.

Patareid ja toide

Patareide pluss läheb Super Mini 5V pinni, miinus GND-sse. 100–470 µF kondensaator on toite ja GND vahel, et flashi kirjutamise vooluimpulss akut ei vajutaks.
Kondensaatori pikem jalg (+) läheb plussi poole (elektrolüütkondensaatoril on miinusmärgiga triip).

DS18B20

Punane 3V3, must GND, kollane (data) GPIO4.
4,7 kΩ takisti on andmejuhtme ja 3V3 vahel. Jooda see plaadi poolsesse otsa, mitte anduri juurde.
Kui lisad teise anduri (õhk), ühenda selle kolm juhet paralleelselt samadesse punktidesse, takisti jääb ikka ainult üks.

Reed-lüliti / nupp

Üks viik GPIO3, teine GND-sse. Polaarsust pole.
100 kΩ takisti GPIO3 ja 3V3 vahel hoiab pinni ootel kõrgel. Sleep’is voolab sellest ~30 µA ainult siis, kui lüliti on suletud, ehk praktiliselt mitte midagi.
Reed-lüliti pane karbi sisse seina vastu, kus magnet väljast kõige paremini ligi pääseb. Testi enne lõplikku paigaldust, kui kaugelt magnet lülitab.

Enne karpi panekut

Eemalda Super Mini punane toite-LED (muidu on sleep-vool ~1 mA).
Kontrolli multimeetriga, et GND-id on ühendatud ja 3V3 ja GND vahel pole lühist.
Mõõda sleep-vool, soovitavalt alla 300 µA.


<img width="1455" height="1159" alt="image" src="https://github.com/user-attachments/assets/fbc8849f-e372-4332-9a40-68a3d4985f51" />
Uus eskiis on ülal. Moodul on nüüd plaadi vasakus servas ja antenn ulatub servast välja. Selle ümber on vaba ala.

Mis muutus
J1 pesa on plaadi vasakus servas (veerud 5 ja 6). Mooduli keha jääb pesast vasakule ja antenn plaadist välja (~1 cm).
T1, C1 ja U1 on kõik all paremal. Ülemisel poolel pole ühtegi kõrget osa ega klemmi.
T2 (andur) ja T3 (reed) on samuti all.
Mooduli all on ainult R2 ja R4 (madalad takistid) ning mõned juhtmed alumisel poolel. Need ei jää antenni kohale.
3V3 jookseb üles mööda vertikaalset juhet (veerg 11) ja sealt plaadi ülaääres vasakule R2 ja R4 jaoks.
Juhtmed ristuvad kolmes kohas (ringid). Kasuta isoleeritud juhet.
Kontrolli enne jootmist
J1 pesa järjekord on sinu kinnitusel õige: vasak veerg RX, GPIO0, GPIO2, GND ja parem veerg VCC, RST, CH_PD, TX. Moodul läheb pessa nii, et antenn on vasakul.
U1 SOT-23 adapteril on vasakult paremale GND, OUT, IN. Kontrolli seda andmelehelt (MCP1700 SOT-23A: pin 1 GND, pin 2 VOUT, pin 3 VIN).
T2 vasakult paremale: must (GND), kollane (DATA), punane (3V3).
Karbis

Hoia antenni ümbrus vaba. Pane patareid ja metallosad antennist eemale (vähemalt paar sentimeetrit) ning ära kata antenni teibi, alumiiniumi ega vahtplastiga, mis sisaldab süsi. Plastkarp on okei.

Ehitamise ja testimise järjekord on sama, mis eelmisel korral: kõigepealt toiteosa (mõõda 3,3 V), siis pesa ja takistid (mõõda veel ilma modulita), ja alles lõpus pane ESP-01 pessa.
