MEIN FINANZ-DASHBOARD – PWA-PROTOTYP (Version 0.1)

Enthalten:
- Offlinefähige Web-App mit installierbarem Manifest und Service Worker
- Fünf monatliche Budgets mit positiven und negativen Überträgen ab November 2026
- Buchungen mit Pflicht-Personenzuordnung und Aufteilung auf mehrere Kategorien/Budgets/Personen
- Zahlungsdatum getrennt vom Ausgabedatum; offene und bestätigte Zahlungen
- Wiederkehrende monatliche Termine; Konto-Prognose 60 Tage und 500-Euro-Warnschwelle
- Fünf ING-Rücklagen plus Girokonto; Umbuchungen; manueller Kontostandsabgleich
- JSON-Sicherung/Wiederherstellung, CSV-Buchungsexport

WICHTIG: Dies ist eine erste Testversion. Nicht alle Werte der Excel-Datei sind bereits als Zahlungstermine hinterlegt. Die fünf Budgets und Rücklagenbezeichnungen/Planraten wurden als Grundlage übernommen. Anfangsguthaben sind absichtlich 0 Euro, bis du echte Stände eingibst.

STARTEN / TESTEN
1. ZIP-Datei entpacken.
2. Auf dem PC mit Python (falls vorhanden) im entpackten Ordner starten:
   python -m http.server 8000
3. Im PC-Browser http://localhost:8000 aufrufen.
4. Zur Installation auf dem Android-Smartphone müssen die Dateien über HTTPS bereitgestellt werden. Erst dann im Browser "Zum Startbildschirm hinzufügen" bzw. "App installieren" auswählen. Ein lokaler PC-Server ist vom Handy aus nicht automatisch installierbar.

DATENSCHUTZ
- Daten bleiben im lokalen Browser-Speicher (localStorage), kein Bankzugriff, keine Server-API.
- JSON-Export ist derzeit NICHT verschlüsselt. Datei geschützt aufbewahren.
- Browserdaten löschen / Browser wechseln kann lokale Daten entfernen. Regelmäßig exportieren!
- Fotos/PDFs können ausgewählt, aber noch nicht verarbeitet oder gespeichert werden.
- Erinnerungen als Android-Benachrichtigungen und Drive-Sicherung sind noch nicht implementiert.

BEKANNTE EINSCHRÄNKUNGEN
- Zahlungen aus Excel müssen für die Liquiditätsrechnung einmalig als regelmäßige Termine ergänzt werden.
- Konto-Startstände sind Stichtagswerte. Die App summiert bestätigte Buchungen ab diesem Datum.
- Bei manueller Eingabe muss man Doppelbuchungen vermeiden.
- Eine automatische monatliche Sparplan-Umbuchung zwischen zwei Konten ist noch nicht vorhanden.
- Ein Teil der Budgetplan-Einnahmen wird nicht als Termine vorbelegt, um keine falsche Prognose zu erzeugen.
- Die App ist ein Prototyp, keine geprüfte Buchhaltungssoftware.
