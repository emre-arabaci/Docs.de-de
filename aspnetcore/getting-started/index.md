---
title: Erste Schritte mit ASP.NET Core
author: rick-anderson
description: Kurztutorial, in dem eine einfache Hello World-App mit ASP.NET Core erstellt und ausgeführt wird.
ms.author: riande
ms.custom: mvc
ms.date: 01/15/2019
uid: getting-started
ms.openlocfilehash: eee927f4306fa7757f3f361e6c6f367658512897
ms.sourcegitcommit: 42a8164b8aba21f322ffefacb92301bdfb4d3c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341809"
---
# <a name="tutorial-get-started-with-aspnet-core"></a>Tutorial: Erste Schritte mit ASP.NET Core

Dieses Tutorial zeigt, wie die .NET Core-Befehlszeilenschnittstelle verwendet wird, um eine ASP.NET Core-Web-App zu erstellen.

Sie lernen, die folgende Aufgaben auszuführen:

> [!div class="checklist"]
> * Erstellen Sie ein Web-App-Projekt.
> * Aktivieren Sie lokales HTTPS.
> * Führen Sie die App aus.
> * Bearbeiten Sie eine Razor-Seite.

Am Schluss werden Sie eine funktionierende Web-App auf Ihrem lokalen Computer besitzen.

![Web-App-Startseite](_static/home-page.png)

## <a name="prerequisites"></a>Erforderliche Komponenten

* [.NET Core 2.2 SDK](https://www.microsoft.com/net/download/all)

## <a name="create-a-web-app-project"></a>Erstellen Sie ein Web-App-Projekt.

Öffnen Sie eine Befehlsshell, und geben Sie den folgenden Befehl ein:

```console
dotnet new webapp -o aspnetcoreapp
```

## <a name="enable-local-https"></a>Aktivieren Sie lokales HTTPS.

Vertrauen Sie dem HTTPS-Entwicklungszertifikat:

# <a name="windowstabwindows"></a>[Windows](#tab/windows)

```console
dotnet dev-certs https --trust
```

Über den vorherigen Befehl wird der folgende Dialog angezeigt:

![Dialogfeld „Sicherheitswarnung“](_static/cert.png)

Klicken Sie auf **Ja**, wenn Sie zustimmen möchten, dass das Entwicklungszertifikat vertrauenswürdig ist.

# <a name="macostabmacos"></a>[macOS](#tab/macos)

```console
dotnet dev-certs https --trust
```

Über den vorherigen Befehl wird die folgende Meldung angezeigt:

*Trusting the HTTPS development certificate was requested. Wenn das Zertifikat nicht bereits vertrauenswürdig, ist führen wir den folgenden Befehl aus:*  `'sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain <<certificate>>'`.  
*Dieser Befehl fordert Sie möglicherweise zur Eingabe Ihres Kennworts auf, um das Zertifikat für die Systemkeychain zu installieren.

Kennwort:*

Geben Sie Ihr Kennwort ein, wenn Sie die Vertrauenswürdigkeit des Entwicklungszertifikats bestätigen möchten.

# <a name="linuxtablinux"></a>[Linux](#tab/linux)

Weitere Informationen zum Bestätigen der Vertrauenswürdigkeit eines HTTPS-Entwicklungszertifikats finden Sie in der Dokumentation zu Ihrer Linux-Distribution.

---

## <a name="run-the-app"></a>Ausführen der App

Führen Sie die folgenden Befehle aus:

```console
cd aspnetcoreapp
dotnet run
```

Nachdem die Befehlsshell angibt, dass die App gestartet wurde, wechseln Sie zu [https://localhost:5001](https://localhost:5001). Klicken Sie auf **Accept** (Akzeptieren), um die Datenschutz- und Cookierichtlinie zu akzeptieren. Diese App bewahrt keine personenbezogenen Informationen auf.

## <a name="edit-a-razor-page"></a>Bearbeiten einer Razor-Seite

Öffnen Sie *Pages/Index.cshtml*, und ändern Sie die Seite mit dem folgenden hervorgehobenen Markup:

[!code-cshtml[](sample/index.cshtml?highlight=9)]

Navigieren Sie zu [https://localhost:5001](https://localhost:5001), und überprüfen Sie, ob die Änderungen angezeigt werden.

## <a name="next-steps"></a>Nächste Schritte

In diesem Tutorial haben Sie gelernt, wie die folgenden Aufgaben ausgeführt werden:

> [!div class="checklist"]
> * Erstellen Sie ein Web-App-Projekt.
> * Aktivieren Sie lokales HTTPS.
> * Führen Sie das Projekt aus.
> * Führen Sie eine Änderung durch.

Um mehr über ASP.NET Core zu lernen, lesen Sie die Einleitung:

> [!div class="nextstepaction"]
> <xref:index>
