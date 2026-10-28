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
