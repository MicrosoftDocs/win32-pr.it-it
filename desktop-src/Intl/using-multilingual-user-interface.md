---
description: Uso dell'interfaccia utente multilingue
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Uso dell'interfaccia utente multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234192"
---
# <a name="using-multilingual-user-interface"></a>Uso dell'interfaccia utente multilingue

Questa sezione descrive come usare la funzionalità Multilingual User Interface (MUI) per progettare e implementare le applicazioni. Di seguito sono riportati alcuni aspetti della tecnologia MUI che entrano in gioco alla maggior parte delle fasi del ciclo di vita dell'applicazione.

-   Sviluppo di applicazioni, tra cui la preparazione delle risorse, l'impostazione delle preferenze della lingua dell'applicazione, la ricerca e il caricamento delle risorse
-   Compilazione e localizzazione dell'applicazione
-   Distribuzione dell'applicazione

Di seguito sono riportate alcune domande da considerare durante la progettazione e l'implementazione di un'applicazione MUI.

-   Quali sono le versioni di Windows supportate dall'applicazione?
-   In quali lingue verrà localizzata l'applicazione?
-   Se le impostazioni della lingua dell'applicazione seguono sempre le impostazioni della lingua per il sistema operativo o se l'utente dell'applicazione è in grado di impostare lingue specifiche?
-   Quali tipi di risorse dell'interfaccia utente vengono utilizzate dall'applicazione e dove vengono archiviati?

Questa sezione include gli argomenti seguenti. Le descrizioni presuppongono che un'applicazione MUI sia destinata a Windows Vista e versioni successive. Le risorse per questa applicazione sono risorse Win32, con risorse specifiche del linguaggio e codice eseguibile che risiede in file PE Win32 distinti. Considerazioni speciali per il supporto dei sistemi operativi precedenti a Windows Vista o per i diversi tipi di risorse vengono aggiunti a seconda delle esigenze.

-   [Preparazione delle risorse](preparing-resources.md)
-   [Impostazione delle preferenze di lingua dell'applicazione](setting-application-language-preferences.md)
-   [Individuazione delle risorse PE Win32](locating-win32-pe-resources.md)
-   [Individuazione di risorse PE non Win32](locating-non-win32-pe-resources.md)
-   [Localizzazione delle risorse e compilazione dell'applicazione](localizing-resources-and-building-the-application.md)
-   [Esempio di applicazione delle impostazioni di sistema MUI:](mui-system-settings-application-sample.md)
-   [Esempio di impostazioni di MUI: Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
-   [Esempio di impostazioni di MUI: Application-Specific (precedente a Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)

 

 



