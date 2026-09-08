# Taste Profile

MASTERPROMPT – FOOD4YOU PERSONALISIERUNG / REZEPT-EMPFEHLUNGSALGORITHMUS

WICHTIG:

Baue in die BESTEHENDE Food4You-App ein regelbasiertes Empfehlungssystem als Ersatz für einen klassischen KI-/Machine-Learning-Algorithmus.

Das Ziel ist NICHT, eine echte KI zu implementieren.

Das Ziel ist ein intelligentes, nachvollziehbares Punktesystem, das aus den Präferenzen und dem Verhalten des Users lernt und dadurch den Swipe-/Empfehlungsfeed immer besser personalisiert.

==================================================

1. GOLDENE REGEL – NICHTS BESTEHENDES KAPUTT MACHEN

==================================================

Die bestehende Food4You-App funktioniert bereits und besitzt viele Funktionen.

Diese Funktionen müssen vollständig erhalten bleiben.

NICHT entfernen:

- Entdecken

- Swipe

- Viral

- Favoriten

- Social

- Shopping / Einkaufsliste

- Profil

- Wochenplan

- Rezeptdetails

- Kochmodus

- ähnliche Rezepte

- Premium

- Favoritenlimit

- Rezeptsuche

- bestehende Filter

- bestehende Rezeptdaten

- bestehende Nutrition-Daten

- bestehende Portionenumrechnung

- bestehendes Tracking

- Like

- Skip

- Favorisieren

- „Als gekocht markieren“

- „Zur Einkaufsliste hinzufügen“

- Sammlungen

- Rating

- Navigation

- bestehende State-Logik

- bestehende Detailansichten

- bestehende Swipe-Funktion

Der neue Recommendation-Mechanismus soll sich in die bestehende Architektur integrieren.

Nicht unnötig bestehende Komponenten neu schreiben.

Nicht bestehende Funktionalität ersetzen, wenn sie bereits funktioniert.

==================================================

2. ZIEL

==================================================

Der User soll das Gefühl bekommen:

„Die App versteht langsam, was ich gerne esse.“

Das System soll aus folgenden Dingen lernen:

1. Initiale Präferenzen beim ersten Start

2. Likes

3. Skips

4. Favoriten

5. gekochte Rezepte

6. häufig angesehene Rezepte

7. verwendete Filter

8. Ernährungspräferenzen

9. Kategorien

10. Zutaten

11. Küche / Cuisine

12. Zubereitungsdauer

13. Kalorien

14. Protein

15. Preis/Budget, sofern vorhanden

16. wiederholte Interaktionen

Das System soll NICHT einfach zufällig Rezepte anzeigen.

==================================================

3. INITIALER FRAGEBOGEN BEIM ERSTEN ÖFFNEN

==================================================

Beim ersten Öffnen der App bzw. wenn noch keine Initial Preferences vorhanden sind, soll ein moderner Onboarding-Fragebogen erscheinen.

Der Fragebogen soll NICHT bei jedem App-Start erneut erscheinen.

Nur:

- beim allerersten Start

oder

- wenn noch keine Initial Preferences existieren.

Der User kann die Fragen überspringen.

==================================================

4. ONBOARDING – FRAGE 1

==================================================

Headline:

„Was möchtest du heute essen?“

Mehrfachauswahl möglich.

Optionen:

🍝 Einfach lecker

💪 Proteinreich

🥗 Gesund & ausgewogen

⚡ Schnell & unkompliziert

💰 Günstig

🔥 Etwas Besonderes

🌎 Internationale Küche

🎲 Überrasche mich

Die Auswahl wird gespeichert.

Mehrfachauswahl muss möglich sein.

==================================================

5. ONBOARDING – FRAGE 2

==================================================

Headline:

„Welche Küche magst du?“

Mehrfachauswahl.

Beispiele:

🇮🇹 Italienisch

🇲🇽 Mexikanisch

🇮🇳 Indisch

🇯🇵 Japanisch

🇹🇭 Thai

🇺🇸 Amerikanisch

🇬🇷 Griechisch

🇹🇷 Türkisch

🇨🇳 Chinesisch

🇪🇸 Spanisch

🥘 Mediterran

🍜 Asiatisch

🍽️ Deutsch

🌎 Egal / alles

Die Auswahl wird gespeichert.

==================================================

6. ONBOARDING – FRAGE 3

==================================================

Headline:

„Wie wichtig ist dir eine schnelle Zubereitung?“

Optionen:

⚡ Sehr wichtig

🙂 Eher wichtig

😐 Egal

🍳 Ich nehme mir gerne Zeit

Daraus wird ein Zeit-Personalisierungswert erstellt.

==================================================

7. ONBOARDING – FRAGE 4

==================================================

Headline:

„Was ist dir bei Ernährung wichtig?“

Mehrfachauswahl:

💪 Viel Protein

🔥 Kalorienbewusst

🥗 Ausgewogen

🥑 Wenig Fett

🍚 Weniger Kohlenhydrate

🌱 Vegetarisch

🌿 Vegan

🥩 Fleisch

🐟 Fisch

😌 Keine besonderen Vorgaben

Die Auswahl darf NICHT andere bestehende Ernährungsfunktionen überschreiben.

==================================================

8. ONBOARDING – FRAGE 5

==================================================

Headline:

„Wie viel möchtest du ungefähr ausgeben?“

Optionen:

💰 Günstig

💶 Normal

💎 Egal

Nur verwenden, wenn für das Rezept eine Preis-/Budget-Schätzung vorhanden ist.

Wenn keine Preisdaten vorhanden sind:

Preis nicht als negativer Faktor verwenden.

==================================================

9. ONBOARDING – ABSCHLUSS

==================================================

Button:

„Meine Rezepte entdecken“

Danach:

→ Swipe-Tab bzw. bestehender Startbereich.

Die Antworten werden als INITIAL PREFERENCES gespeichert.

==================================================

10. SCORING-SYSTEM

==================================================

Jedes Rezept bekommt vor der Anzeige einen dynamischen Recommendation Score.

Beispiel:

BASE SCORE = 50

Danach werden Punkte addiert oder abgezogen.

Wichtig:

Das System soll nicht nur einen einzigen Faktor betrachten.

Mehrere Faktoren sollen kombiniert werden.

==================================================

11. KATEGORIE-SCORE

==================================================

Wenn ein Rezept zu einer vom User bevorzugten Kategorie passt:

+8

Starke Übereinstimmung:

+12

Keine Präferenz:

0

Nicht passende Kategorie:

-5

==================================================

12. CUISINE-SCORE

==================================================

Bevorzugte Küche:

+8

Sehr häufig gelikte Küche:

+12

Neutrale Küche:

0

Wiederholt übersprungene Küche:

-6

==================================================

13. LIKE

==================================================

Wenn der User ein Rezept liked:

Das Rezept:

+15

Ähnliche Rezepte:

+5 bis +8

Ähnliche Kategorie:

+3

Ähnliche Cuisine:

+3

Ähnliche Hauptzutaten:

+2 bis +5

Dadurch soll der Algorithmus aus Likes lernen.

==================================================

14. SKIP

==================================================

Wenn der User ein Rezept bewusst wegwischt:

Rezept:

-15

Ähnliche Rezepte:

-5

Ähnliche Kategorie:

-3

Ähnliche Cuisine:

-3

Wenn der User dieselbe Kategorie mehrfach skipped:

zusätzlicher Malus bis maximal:

-10

Nicht übertreiben.

Ein einzelner Skip darf nicht dafür sorgen, dass eine komplette Kategorie dauerhaft verschwindet.

==================================================

15. FAVORITEN

==================================================

Wenn ein Rezept favorisiert wird:

+20

Ähnliche Rezepte:

+8

Ähnliche Kategorie:

+5

Ähnliche Cuisine:

+5

Ähnliche Hauptzutaten:

+3

Favorisieren ist ein stärkeres positives Signal als ein einfacher Like.

==================================================

16. GEKOCHTE REZEPTE

==================================================

Wenn ein Rezept als „gekocht“ markiert wird:

+20

Ähnliche Rezepte:

+8

Ähnliche Kategorie:

+5

Ähnliche Zutaten:

+3

Gekochte Rezepte sind ein sehr starkes positives Interesse-Signal.

==================================================

17. REZEPTDETAILS ANGESEHEN

==================================================

Wenn der User ein Rezept öffnet:

+2

Wenn der User längere Zeit auf einem Rezept bleibt:

zusätzlicher kleiner Bonus.

Aber:

Das Öffnen alleine darf kein starkes Signal sein.

Likes/Favoriten/gekocht haben deutlich mehr Gewicht.

==================================================

18. WIEDERHOLTE INTERAKTION

==================================================

Wenn ein User wiederholt mit ähnlichen Rezepten interagiert:

verstärke die entsprechende Präferenz.

Beispiel:

User liked:

Pasta

Pasta

Pasta

Lasagne

Pesto-Pasta

Dann soll „Italienisch / Pasta“ automatisch stärker gewichtet werden.

Nicht zwingend eine neue Preference anzeigen.

Einfach intern stärker gewichten.

==================================================

19. ZEIT-PERSONALISIERUNG

==================================================

Wenn der User bevorzugt schnelle Rezepte auswählt:

Rezepte bis 30 Minuten:

+8

Rezepte bis 20 Minuten:

+10

Rezepte über 60 Minuten:

-5

Wenn der User „Ich nehme mir gerne Zeit“ auswählt:

lange Rezepte dürfen keinen Malus bekommen.

==================================================

20. NUTRITION-SCORE

==================================================

Nutrition-Daten sollen für Empfehlungen verwendet werden.

Wenn User „Proteinreich“ bevorzugt:

hohes Protein:

+10

sehr hohes Protein:

+12

niedriges Protein:

-3

Wenn User „Kalorienbewusst“ bevorzugt:

niedrige/moderate Kalorien:

+8

sehr kalorienreiche Rezepte:

-5

WICHTIG:

Nutrition darf nur bewertet werden, wenn Nutrition-Daten vorhanden sind.

Fehlende Daten:

0 Punkte.

Nicht automatisch bestrafen.

==================================================

21. PROTEIN-SCORE

==================================================

Wenn Protein-Daten vorhanden sind:

<15 g:

0

15–25 g:

+3

25–40 g:

+7

40–60 g:

+10

>60 g:

+12

Diese Werte gelten als grobe Recommendation-Signale.

Nicht als medizinische Aussage verwenden.

==================================================

22. BUDGET-SCORE

==================================================

Wenn Preis-/Budgetdaten vorhanden sind:

Günstig + User bevorzugt günstig:

+8

Sehr günstig:

+10

Teuer + User bevorzugt günstig:

-6

Wenn der User „Egal“ auswählt:

0

Wenn kein Preis vorhanden ist:

0

Keine Strafe für fehlende Preisdaten.

==================================================

23. ERNÄHRUNGSPRÄFERENZEN

==================================================

Wenn User vegetarisch ausgewählt hat:

Vegetarische Rezepte:

+10

Nicht vegetarische Rezepte:

starker Malus

Wenn User vegan ausgewählt hat:

Vegane Rezepte:

+12

Nicht vegane Rezepte:

starker Malus

Bestehende Ernährungslogik nicht überschreiben.

==================================================

24. ZUTATEN-PRÄFERENZEN

==================================================

Das System soll aus wiederholten Interaktionen mit Zutaten lernen.

Beispiel:

User liked häufig Rezepte mit:

Hähnchen

Avocado

Tomaten

Mozzarella

Dann:

Hähnchen:

+4

Avocado:

+4

Tomaten:

+2

Mozzarella:

+3

Wenn User wiederholt Rezepte mit einer Zutat skipped:

entsprechender kleiner Malus.

Nicht zu aggressiv.

==================================================

25. CUISINE LEARNING

==================================================

Der Algorithmus soll automatisch erkennen, welche Küchen der User bevorzugt.

Beispiel:

10 Interaktionen:

Italienisch: 7 positive

Mexikanisch: 1 positive

Indisch: 2 positive

Dann bekommt Italienisch einen stärkeren Recommendation Bonus.

==================================================

26. KATEGORIE LEARNING

==================================================

Analog zu Cuisine.

Mögliche Kategorien:

- Pasta

- Bowls

- Burger

- Wraps

- Curry

- Reisgerichte

- Salate

- Ofengerichte

- Suppen

- Street Food

- Frühstück

- Desserts

- etc.

WICHTIG:

Nur Kategorien verwenden, die tatsächlich in den bestehenden Rezeptdaten vorhanden sind.

Keine künstlichen Kategorien erzwingen.

==================================================

27. RECENCY / WIEDERHOLUNGEN

==================================================

Der Feed darf nicht ständig dasselbe Rezept oder fast dasselbe Rezept zeigen.

Wenn ein Rezept gerade angezeigt wurde:

temporär nach unten priorisieren.

Wenn ein Rezept gerade geliked wurde:

ähnliche Rezepte dürfen auftauchen.

Aber:

nicht 10 fast identische Rezepte direkt hintereinander.

==================================================

28. DIVERSITY

==================================================

Der Algorithmus darf nicht zu „eng“ werden.

Beispiel:

User liked 5 Pasta-Rezepte.

Dann sollen nicht ausschließlich Pasta-Rezepte erscheinen.

Etwa:

70–80 % stark personalisierte Empfehlungen

20–30 % Discovery / Exploration

Damit der User weiterhin neue Gerichte entdeckt.

==================================================

29. EXPLORATION

==================================================

Ein Teil des Feeds soll bewusst neue Inhalte enthalten.

Beispiel:

User mag italienisch.

Trotzdem gelegentlich:

japanisch

mexikanisch

indisch

griechisch

anzeigen.

Wenn der User diese ebenfalls liked:

Preference entsprechend erhöhen.

Wenn er sie skipped:

Preference entsprechend reduzieren.

So lernt das System.

==================================================

30. SCORE-FORMEL

==================================================

Die finale Bewertung soll ungefähr nach diesem Prinzip funktionieren:

FINAL SCORE =

BASE SCORE

+ Preference Score

+ Cuisine Score

+ Category Score

+ Like Similarity Score

+ Favorite Similarity Score

+ Cooked Similarity Score

+ Ingredient Score

+ Nutrition Score

+ Time Score

+ Budget Score

+ Interaction Score

+ Recency/Interest Score

- Skip Penalties

- Repetition Penalties

Danach:

Exploration Bonus für einen Teil der Rezepte.

==================================================

31. SCORE NORMALISIEREN

==================================================

Verhindere extreme Werte.

Der Score sollte intern normalisiert werden.

Beispielsweise:

0–100

oder eine technisch sinnvolle vergleichbare Skala.

Wichtig ist nicht die exakte Zahl.

Wichtig ist die korrekte relative Reihenfolge.

==================================================

32. SWIPE FEED

==================================================

Der Swipe Feed soll nicht einfach die Rezeptdatenbank in fester Reihenfolge anzeigen.

Stattdessen:

1. verfügbare Rezepte laden

2. Rezepte filtern

3. jedes Rezept bewerten

4. Scores berechnen

5. sortieren

6. Diversity berücksichtigen

7. bereits gesehene Rezepte berücksichtigen

8. Feed generieren

Der User soll dadurch einen personalisierten Feed erhalten.

==================================================

33. FILTER

==================================================

Wenn der User einen Filter verwendet:

Dieser Filter hat Priorität.

Beispiel:

„Proteinreich“

Dann dürfen nur passende Rezepte bzw. die dafür vorgesehenen Ergebnisse erscheinen.

Wenn kein Filter aktiv ist:

Der gesamte verfügbare Rezeptbestand darf grundsätzlich verwendet werden.

Nicht künstlich auf z. B. 30 Rezepte beschränken.

Es soll sich wie ein praktisch endloser Feed anfühlen.

==================================================

34. KEIN ENDLICHER 30-REZEPTE-FEED

==================================================

Wenn genügend Rezepte vorhanden sind:

Der User soll theoretisch sehr lange weiterswipen können.

Wenn der Feed seine erste Gruppe verarbeitet hat:

automatisch weitere geeignete Rezepte nachladen.

Keine harte Grenze von 30 Rezepten.

Keine Meldung wie:

„Keine weiteren Rezepte“

wenn in der Datenbank noch geeignete Rezepte vorhanden sind.

==================================================

35. USER-PROFIL / PREFERENCES

==================================================

Die gelernten Präferenzen sollen NICHT zwingend direkt sichtbar sein.

Intern speichern:

- bevorzugte Kategorien

- bevorzugte Cuisines

- bevorzugte Zutaten

- bevorzugte Nutrition-Eigenschaften

- bevorzugte Zubereitungsdauer

- Budgetpräferenz

- positive Interaktionen

- negative Interaktionen

Bestehende Profilfunktionen nicht verändern.

==================================================

36. RESET

==================================================

Der User soll nicht dauerhaft in einem schlechten Recommendation State gefangen sein.

Wenn bereits bestehende Einstellungen oder ein Logout-/Login-System vorhanden sind:

Recommendation-Daten sauber dem jeweiligen User zuordnen.

Bei Logout:

keine Vermischung verschiedener Accounts.

Bei neuem User:

neuer Recommendation State.

Bestehende Account-/Cloud-Sync-Logik nicht beschädigen.

==================================================

37. GUEST USER

==================================================

Falls die App bereits Guest-/LocalStorage-Logik besitzt:

Recommendation State entsprechend namespacen.

Guest-Verhalten darf nicht versehentlich mit einem eingeloggten User vermischt werden.

Bestehende Storage-Architektur verwenden.

Keine neue parallele Storage-Architektur erstellen, wenn nicht notwendig.

==================================================

38. PERFORMANCE

==================================================

Das Scoring darf den Swipe-Feed nicht verlangsamen.

Keine sichtbaren Verzögerungen beim Swipen.

Keine Berechnung soll dazu führen, dass:

- Karten springen

- Bilder später erscheinen

- Swipe ruckelt

- UI einfriert

Scores möglichst effizient berechnen und geeignete Daten cachen.

==================================================

39. BESTEHENDE SWIPE-UI NICHT VERÄNDERN

==================================================

Der Algorithmus soll die REIHENFOLGE der Rezepte bestimmen.

Er soll NICHT die bestehende Swipe-UI ersetzen.

Bestehende Swipe-Karte behalten.

Bestehende Informationen behalten:

- Rezeptname

- Bild

- Kategorie

- Dauer

- Kalorien

- Protein/Nutrition, sofern aktuell angezeigt

- vegetarisch/vegan

- Influencer

- Viral

- weitere bestehende Badges

- weitere bestehende Informationen

Keine Informationen entfernen.

==================================================

40. SWIPE-INTERAKTIONEN

==================================================

Bestehende Interaktionen bleiben erhalten:

RECHTS:

Like

LINKS:

Skip

BILD ANTIPPEN:

Details

Diese Aktionen müssen gleichzeitig als Recommendation Signals verwendet werden.

==================================================

41. FEEDBACK LOOP

==================================================

Beispiel:

User sieht:

Chicken Teriyaki

→ öffnet Details

→ liked

Dann soll das System lernen:

+ Chicken

+ asiatisch

+ Reis

+ proteinreich

+ entsprechende Kategorie

Wenn danach:

Chicken Bowl

kommt:

höhere Wahrscheinlichkeit.

Wenn:

Vegane Bohnen-Linsen-Suppe

kommt:

je nach bisherigem Verhalten entsprechend bewerten.

==================================================

42. NICHT ÜBERPERSONALISIEREN

==================================================

Ein einzelner Like darf nicht den gesamten Feed verändern.

Ein einzelner Skip darf nicht eine komplette Kategorie eliminieren.

Das System soll mit zunehmenden Interaktionen immer besser werden.

Frühe Interaktionen:

geringere Sicherheit.

Viele Interaktionen:

höhere Sicherheit.

==================================================

43. COLD START

==================================================

Bei einem neuen User:

Onboarding Preferences verwenden.

Wenn der User den Fragebogen überspringt:

allgemein beliebte / diverse Rezepte verwenden.

Danach:

Likes/Skips/Favoriten etc. verwenden.

==================================================

44. VIRAL TAB

==================================================

Der Viral Tab bleibt funktional unabhängig.

Der Recommendation-Algorithmus darf dort NICHT einfach die Viral-Rezepte entfernen.

Falls Personalisierung dort bereits existiert:

nur verbessern.

Viral muss weiterhin Viral-/Influencer-Rezepte anzeigen.

==================================================

45. ENTDECKEN TAB

==================================================

Entdecken bleibt funktional wie bisher.

Suche und Filter bleiben erhalten.

Der Recommendation Score darf die Darstellung dort nicht kaputtmachen.

Wenn Entdecken bereits eine eigene Sortierung besitzt:

diese nicht einfach ersetzen.

==================================================

46. PREMIUM

==================================================

Premium bleibt vollständig bestehen.

Der Recommendation-Algorithmus darf keine bestehenden Premium-Funktionen entfernen.

Keine neue Bezahlschranke hinzufügen.

==================================================

47. DATENSTRUKTUR

==================================================

Wenn möglich, Recommendation-Daten strukturiert speichern.

Beispielsweise:

userPreferences

categoryScores

cuisineScores

ingredientScores

nutritionPreferences

timePreference

budgetPreference

likedRecipes

skippedRecipes

favoriteRecipes

cookedRecipes

viewedRecipes

recentlyShown

WICHTIG:

Bestehende Datenstrukturen zuerst analysieren.

Nicht unnötig neue parallele Systeme erstellen.

==================================================

48. DEBUG / TEST

==================================================

Nach Implementierung testen:

TEST 1:

Neuer User öffnet App.

→ Onboarding erscheint.

TEST 2:

User wählt:

Proteinreich

Schnell

Italienisch

→ Feed priorisiert entsprechende Rezepte.

TEST 3:

User liked mehrere Pasta-Rezepte.

→ ähnliche Pasta-/italienische Rezepte steigen im Score.

TEST 4:

User skipped mehrere Rezepte einer Kategorie.

→ diese Kategorie wird etwas weniger priorisiert.

TEST 5:

User favorisiert mehrere Rezepte.

→ ähnliche Rezepte werden stärker priorisiert.

TEST 6:

User markiert mehrere Rezepte als gekocht.

→ ähnliche Rezepte erhalten Bonus.

TEST 7:

User nutzt keinen Filter.

→ gesamter verfügbarer Rezeptbestand kann genutzt werden.

TEST 8:

User swiped sehr lange.

→ keine harte Grenze bei 30 Rezepten.

TEST 9:

User loggt aus.

→ Recommendation State wird nicht mit anderem User vermischt.

TEST 10:

Swipe UI bleibt performant.

==================================================

49. WICHTIG – NICHT DIE REZEPTE VERÄNDERN

==================================================

Der Algorithmus darf die vorhandenen Rezeptdaten nicht verändern.

Er bewertet sie lediglich.

Keine Rezepte löschen.

Keine Rezepte duplizieren.

Keine Zutaten verändern.

Keine Mengen verändern.

Keine Nutrition-Werte verändern.

Keine Bilder verändern.

Keine bestehenden Rezeptinformationen verändern.

==================================================

50. ENDZIEL

==================================================

Food4You soll sich durch dieses System zunehmend personalisiert anfühlen.

Am Anfang:

Onboarding bestimmt die erste Richtung.

Nach wenigen Interaktionen:

Likes und Skips beeinflussen den Feed.

Nach vielen Interaktionen:

Kategorien, Cuisines, Zutaten, Nutrition, Zeit und andere Präferenzen werden immer genauer erkannt.

Das Ergebnis soll sich für den User wie ein lernender persönlicher Food-Feed anfühlen.

Wichtig:

KEINE ECHTE KI NOTWENDIG.

Das System soll mit einem intelligenten regelbasierten Scoring-System arbeiten.

Es muss:

SCHNELL

+

STABIL

+

NACHVOLLZIEHBAR

+

ERWEITERBAR

+

PERSONALISIERT

sein.

==================================================

ABSOLUTE PRIORITÄTEN

==================================================

1. Bestehende Funktionen NICHT zerstören.

2. Bestehende Rezeptdaten NICHT verändern.

3. Bestehende Swipe-UI NICHT unnötig umbauen.

4. Swipe muss weiterhin flüssig funktionieren.

5. Onboarding nur beim ersten relevanten Start anzeigen.

6. Likes, Skips, Favoriten und gekochte Rezepte als Lernsignale verwenden.

7. Keine harte 30-Rezepte-Grenze.

8. Ohne Filter grundsätzlich den gesamten verfügbaren Rezeptbestand berücksichtigen.

9. Empfehlungen personalisieren, aber weiterhin abwechslungsreich halten.

10. Performance darf nicht schlechter werden.

==================================================

ABSCHLUSS

==================================================

Implementiere dieses Recommendation-System in die bestehende Food4You-App.

Analysiere zuerst die aktuelle Architektur und integriere das System sauber in die vorhandenen Komponenten.

NICHT alles neu bauen.

NICHT funktionierende Bestandteile ersetzen.

NICHT bestehende Funktionen entfernen.

Das neue System soll sich so anfühlen, als wäre es schon immer Bestandteil von Food4You gewesen.

Das wichtigste Ergebnis:

Der User soll mit jeder Interaktion das Gefühl bekommen:

„Food4You weiß immer besser, was ich essen möchte.“

This project was built with [Lovable](https://lovable.dev).

**Live app**: https://foodswip3r.lovable.app

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/77ec4252-440c-4c39-82bb-6e760205dd9b).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
