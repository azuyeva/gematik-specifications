# gematik-specifications

Dieses Projekt bietet eine Java-Interpretation der gematik-AFOs, die in diversen gematik-Spezifikationen verteilt sind und durch gematik-Produkttypsteckbriefe querreferenziert werden. Die Umsetzung unterteilt die AFOs in jeweilige Namensräume (Java-Packages) und bietet global entsprechende API-Typen (Interfaces) an.

## Versionierung / Release-Umsetzung

Die Versionsnummern der einzelnen Releases referenzieren einen jeweiligen Stand eines gematik-Releases.
- Die Major-Nummer **1** zeigt den Bezug zur gematik Release 1.5 ORS1 mit Basis-Rollout – Erprobung und Produktivbetrieb.
- Jede Minor-Nummer bezieht sich auf einen bestimmten Dokumentenstand der Produkttypsteckbriefe. Exemplarisch steht **1.0** für eine Umsetzung der ORS-1.5-Dokumente vom 19. Juli 2016.
- Die Patch-Nummer repräsentiert den Programmierumfang des Projekts und kann den jeweiligen Release-Notes entnommen werden. 

| Version gematik-specifications |                              Umsetzung von gematik-Release                             |                                           Version Produkttypsteckbriefe                                          |
|:------------------------------:|:--------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------:|
| 1.0.* (Master-Branch)          | [ORS 1.5](http://www.gematik.de/cms/de/spezifikation/release_1_5_ors1/release_1_5.jsp) | [2016-07-19](http://www.gematik.de/cms/media/dokumente/ors1_release_1_5/ORS1_Produkttypsteckbriefe_20160719.zip) |

## Hinweise für Nutzer der gematik-specifications

Sämtliche konkreten Klassen sind stets gegen passende Interfaces entwickelt. Es wird ganz deutlich darauf hingewiesen, dass diese anstatt der konkreten Typen für sämtliche Methoden-Schnittstellen zu verwenden sind, um an zukünftigen Weiterentwicklungen teilhaben zu können.

Desweiteren sind die gematik-AFOs mit unterschiedlichen Anforderungsleveln versehen. Diese sind grundsätzlich Bestandteil der bereits in den `enum`-Klassen erfassten AFOs. Eine Nichtangabe eines Anforderungslevels impliziert eine *MUSS*-Anforderung. Häufig sind jedoch AFOs erfasst worden ohne deren Anforderungslevel anzugeben, da es sich schlicht nicht aus den Produkttypsteckbriefen bzw. AFO-Titeln herauslesen lässt. Derartige AFOs sind mit einem entsprechenden TODO als Java-Kommentar vermerkt. (Das zur Laufzeit abrufbare Level ist daher ggf. nicht korrekt; In den meisten Fällen handelt es sich bei den gematik-AFOs jedoch um *MUSS*-AFOs.)

## Hinweise für Entwickler der gematik-specifications

Sie sind herzlich eingeladen, selbst zu diesem Projekt beizutragen. Legen Sie sich hierzu einem Fork des Projekts an (shared repository model) arbeiten Sie Ihre Ergänzungen ein und tragen Sie diese als Pull-Request an dieses Projekt heran.
- Bitte beachten Sie die Code-Konventionen. 
- Zudem sind alle `enum`-Konstanten alphabetisch sortiert (plus [Trailing-Komma](http://docs.oracle.com/javase/specs/jls/se8/html/jls-8.html#jls-8.9)), um die Code-Änderungen schneller überblicken zu können.
- Arbeiten Sie stets gegen die Interfaces.
- Jeder Code-Beitrag muss, wenn er eine neue Funktionalität beiträgt, durch einen passenden Test überprüfbar sein.
https://help.github.com/articles/about-pull-requests/
