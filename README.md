# [Entwicklung einer dreistufigen Webanwendung mit ASP.NET 2.0, C#, Spring.Net und NHibernate (2010)](https://stahe.github.io/de-pam-aspnet-juin-2010/)

Dieses Dokument beschreibt Schritt für Schritt die Entwicklung von **SimuPaie**, einer .NET-Anwendung, die zur Simulation der Gehaltsabrechnung von Erziehern entwickelt wurde. Das Ziel ist zweigeteilt: **die Festlegung einer klaren Softwarearchitektur** und **die Implementierung der Lösung unter Verwendung der damals verfügbaren .NET-Technologien**. Insbesondere beschreibt das Dokument eine **dreistufige Architektur**, bestehend aus einer Datenzugriffsebene (DAO), einer Geschäftslogikebene und einer Präsentationsschicht, die alle mithilfe von **Spring IoC** integriert sind.

## Kursziele

Der Zweck dieser Fallstudie ist es, zu demonstrieren, wie eine verwaltbare Webanwendung durch eine klare Trennung der Verantwortlichkeiten entworfen wird:

- **Ebene 1 – DAO**: Zugriff auf die in der Datenbank gespeicherten Daten.
- **Ebene 2 – Business**: Lohn- und Gehaltsabrechnungen sowie Geschäftsregeln.
- **Ebene 3 – UI**: Interaktion mit dem Benutzer und Anzeige der Ergebnisse.
- **Integration** der Ebenen über **.NET-Schnittstellen** und **Abhängigkeitsinjektion mit Spring IoC**.

Das Dokument beschreibt zudem den Verarbeitungszyklus von Benutzeranfragen: Die Anfrage wird von der Anwendung empfangen, bei Bedarf an die Business-Ebene und anschließend an die Datenzugriffsebene weitergeleitet, bevor eine entsprechende Antwort an den Client zurückgesendet wird.

## Nachfolgende Versionen der Anwendung

Die Dokumentation beschränkt sich nicht auf eine einzige Implementierung. Sie bietet verschiedene Varianten von SimuPaie, um unterschiedliche Architektur- und Schnittstellenansätze zu veranschaulichen:

1. eine **ASP.NET-Version mit einem einzigen Modul** und einer einstufigen Architektur;
2. eine entsprechende, mit **Ajax** erweiterte Version;
3. eine **dreistufige ASP.NET-Version** mit **NHibernate** für den Datenzugriff;
4. eine **Multi-View-Version mit einer einzigen Seite**;
5. eine serverseitige, auf **Webservices** ausgerichtete Version;
6. eine ASP.NET-Client-Version, die diesen Dienst nutzt;
7. eine **Multi-View-Version mit mehreren Seiten**;
8. eine Client-Version des Webdienstes;
9. eine dreistufige Variante, die sich stärker auf Spring-Klassen stützt, um die Verwendung von NHibernate zu vereinfachen;
10. eine **FLEX**-Client-Version.

## Voraussetzungen

Dieses Dokument richtet sich an **Fortgeschrittene**. Es werden Grundkenntnisse in folgenden Bereichen vorausgesetzt:
- **ASP.NET**;
- **C# 2008**: Klassen, Schnittstellen, Vererbung, Polymorphismus;
- **Spring IoC / Dependency Injection**;
- **dreistufige Webarchitektur** und das **MVC**-Modell.

## Behandelte Werkzeuge und Technologien

Die Fallstudie basiert auf einer einheitlichen Auswahl an Tools und Frameworks:

- **Visual C# 2008**
- **Visual Web Developer Express 2008**
- **SQL Server Express 2005**
- **Spring.Net / Spring IoC**
- **NHibernate**
- **NUnit** für Unit-Tests.

## Was bietet dieses Repository?

Diese Ressource ist besonders interessant für Leser, die:

- die Implementierung einer **mehrschichtigen Architektur** in einer .NET-Umgebung verstehen möchten;
- sehen möchten, wie man die Ebenen der Präsentation, der Geschäftslogik und des Datenzugriffs **entkoppelt**;
- herausfinden möchten, wie man **Spring.Net** für die Zusammenstellung von Komponenten verwendet;
- die Integration von **NHibernate** in eine ASP.NET-Webanwendung untersuchen möchten;
- einem schrittweisen Lernpfad folgen möchten, der von einer einfachen Version zu produktionsreiferen Versionen führt.


## Kursinhalte

Das Dokument skizziert die allgemeine Architektur der Anwendung und veranschaulicht ab der ersten Seite anhand eines Diagramms die Rollen des Benutzers, der Anwendung, der drei Schichten und von Spring IoC bei der Orchestrierung des gesamten Systems. Es dient somit sowohl als **Architekturkurs** als auch als **Entwurfsleitfaden** und als **operative Grundlage für die praktische Umsetzung**.

