# Rust-Editor-mit-VS-Code-Plugin


Projektname: TCP-basierte Client-Server-Kommunikation mit Rust und Node.js
1. Projektbeschreibung
Dieses Projekt implementiert eine einfache Client-Server-Anwendung, bei der ein Server in Rust läuft und ein Client in Node.js (JavaScript) ausgeführt wird. Die beiden Komponenten kommunizieren über eine TCP-Verbindung. Das Hauptziel des Projekts ist es, die Grundlagen der Netzwerkprogrammierung und die Interoperabilität zwischen verschiedenen Programmiersprachen (Rust und JavaScript) zu demonstrieren.

Der Server wartet auf eingehende TCP-Verbindungen, sendet eine vordefinierte Nachricht an den Client und beendet anschließend die Verbindung. Der Client stellt eine Verbindung zum Server her, empfängt die Nachricht, zeigt diese an und schließt die Verbindung.

2. Ziele und Motivation
Netzwerkprogrammierung verstehen: Vermittlung der grundlegenden Konzepte von TCP-Sockets in Rust und Node.js.

Interprozesskommunikation: Erlernen, wie zwei unterschiedliche Systeme auf unterschiedlichen Plattformen über ein Netzwerkprotokoll kommunizieren.

Fehlerbehandlung und Debugging: Umgang mit typischen Problemen wie ungültigen UTF-8-Daten, Verbindungsabbrüchen und Pufferverwaltung.

Projektstrukturierung: Aufbau einer klar getrennten Projektstruktur für Client und Server, jeweils mit den passenden Tools und Umgebungen.

Praxisnähe: Vorbereitung auf komplexere verteilte Systeme und Microservices.


Part 2 : Personal challenges


Dieses Projekt besteht aus einem Rust-Server und einem JavaScript-Client, die über eine TCP-Verbindung kommunizieren. Das Ziel war, eine einfache Nachricht zwischen Client und Server auszutauschen und so die Grundlagen der Netzwerkprogrammierung in Rust und Node.js zu verstehen und umzusetzen.

Herausforderungen und Fehler
Ungültige UTF-8-Sequenz Fehler

Beschreibung: Beim Versuch, Nachrichten zu lesen, trat ein Fehler "Invalid UTF-8 sequence" auf, weil die gelesenen Bytes nicht korrekt als UTF-8 interpretiert werden konnten.

Lösung: Ich habe darauf geachtet, dass Nachrichten immer als gültige UTF-8-Strings gesendet und empfangen werden. Außerdem habe ich sichergestellt, dass der Puffer richtig gefüllt und verarbeitet wird.

Wo soll der Code abgelegt werden?

Herausforderung: Ich war unsicher, in welchem Ordner (z.B. vscodeRustIntegration oder master_editor) die Dateien abgelegt werden sollen, damit die Programme korrekt laufen.

Lösung: Ich habe mich entschieden, den Rust-Server im eigenen Projektordner mit Cargo-Struktur zu haben, und den Client-Code separat im master_editor-Ordner zu speichern, da es sich um unterschiedliche Umgebungen handelt.

Probleme bei der Verbindung und Kommunikation

Beschreibung: Es gab Warnungen und Fehlermeldungen beim Verbindungsaufbau und beim Zugriff auf Ressourcen, z.B. in VSCode-Terminal oder bei Konfigurationszugriffen.

Lösung: Diese Warnungen betrafen hauptsächlich VSCode-Einstellungen und haben die Kommunikation zwischen Client und Server nicht blockiert. Ich habe sie ignoriert und mich auf die funktionierende TCP-Kommunikation konzentriert.

Lösungen Schritt für Schritt
Rust-Server so programmiert, dass er auf TCP-Verbindungen wartet, eine Nachricht sendet und dann die Verbindung sauber schließt.

Node.js-Client geschrieben, der sich mit dem Server verbindet, die Nachricht empfängt, ausgibt und die Verbindung beendet.

UTF-8-Fehler durch kontrolliertes Senden und Empfangen von UTF-8-kodierten Nachrichten vermieden.

Projektstruktur klar getrennt zwischen Server (Rust) und Client (Node.js).

Debugging und Logs genutzt, um Verbindungsstatus und Fehler besser zu verstehen.

Noch vorhandene Schwächen
Der Server akzeptiert nur eine Verbindung und beendet sich dann; für einen produktiven Server wäre ein Mehrfachverbindungs-Handling notwendig.

Fehlendes Fehler-Handling für Netzwerkunterbrechungen und unvorhergesehene Eingaben.

Die Kommunikation ist sehr einfach und nicht verschlüsselt oder gesichert.

Keine automatische Wiederverbindung oder Zeitüberschreitungen implementiert.

Kreative Ansätze
Kombination von Rust und Node.js für eine Client-Server-Architektur genutzt, um unterschiedliche Technologien zu verbinden.

Schrittweises Debuggen mit einfachen Nachrichten, um schrittweise Probleme mit UTF-8 und Verbindungsmanagement zu lösen.

Nutzung von VSCode-Terminals und macOS-Terminal parallel für unterschiedliche Umgebungen und Prozesse.

Selbstständiges Recherchieren und Lösen von Rust-spezifischen String- und Socket-Problemen.

