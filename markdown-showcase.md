# Stammbaum
## **1. Ursprung (Ureltern)**
* Chaos (Urzustand des Universums)
  * Gaia (Erde)
  * Uranos (Himmel)

## **2. Titanen-Generation (Großeltern von Hades)**
* Gaia + Uranos
  * Kronos (Zeit)
  * Rhea (Fruchtbarkeit, Muttergöttin)

## **3. Olympische Götter-Generation (Eltern & Geschwister)**
* Kronos + Rhea
  * Hestia (Herdfeuer)
  * Demeter (Ernte)
  * Hera (Ehe)
  * Hades (Unterwelt)
  * Poseidon (Meer)
  * Zeus (Himmel)

*Kronos verschlang alle Kinder, aber Zeus befreite sie später.*

## **4. [Hades + Persephone](https://www.webtoons.com/de/romance/lore-olympus/list?title_no=2589)** (Tochter von Demeter + Zeus)
*Keine bekannten Kinder in der klassischen Mythologie, da von einer Unfrachtbarkeit Hades' berichtet wird.*

## **5. Haustier (ehrenhalber erwähnt)**

* ![Cerberus](https://static3.cbrimages.com/wordpress/wp-content/uploads/2019/10/Lore-Olympus-feature.jpg) – Der dreiköpfige Höllenhund, Wächter der Unterwelt (nicht verwandt, aber wichtig!)

## **6. Neffen und Nichten**
| Zeus | Poseidon | Demeter | Hera (ohne Zeus) |
|------|----------|---------|------------------|
| Athene| Triton | Persephone | Eileithyia     |
| Apollo | Theseus |        | Hephaistos |
| Artemis | Polyphem|
| Ares |
| Hermes |
| Dionysos |
| Persephone |
| Hebe |
| Herakles |


# Ab ins Reich der Toten - Schritt für Schritt-Anleitung
- [ ] Sterben
- [ ] Münze unter Zuge legen lassen
- [ ] Fahrt im Acheron
- [ ] Hermes geleitet zum Ufer des Styx
- [ ] Überfahrt mit Charon (Obolos zuvor bezahlen)
- [ ] Überprüfung durch Cerberus auf Lebenszeichen

```
class Soul:
    def __init__(self, name, cause_of_death):
        self.name = name
        self.cause_of_death = cause_of_death
        self.location = "River Styx"
    def __str__(self):
        return f"{self.name} (verstorben durch {self.cause_of_death}) – befindet sich bei {self.location}"
class Hades:
    def __init__(self):
        self.souls = []
        self.cerberus_fed = False
        print("Willkommen in der Unterwelt.")
    def welcome_soul(self, soul):
        print(f"👻 Neue Seele empfangen: {soul.name}")
        self.souls.append(soul)
    def feed_cerberus(self):
        self.cerberus_fed = True
        print("🐶 Cerberus wurde gefüttert. Die Seelen sind (vorerst) sicher.")
    def list_souls(self):
        if not self.souls:
            print("Keine Seelen derzeit. Ruhe herrscht.")
        else:
            print("🧟‍♂️ Aktuelle Seelen im Totenreich:")
            for soul in self.souls:
                print(f" - {soul}")
```
