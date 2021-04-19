---
description: Nella procedura seguente viene descritto come abilitare la traccia e la registrazione del debug.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Come abilitare la traccia o la registrazione del debug per MSPs derivati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3883d12c050f245cc58595c9a52586c4f01ba27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308608"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Come abilitare la traccia o la registrazione del debug per MSPs derivati

Assicurarsi prima di tutto che l'implementazione dell'MSP derivato abbia seguito le linee guida riportate nella sezione precedente per quanto riguarda la traccia di debug (definendo il simbolo del preprocessore MSPLOG, la registrazione per la traccia durante DllMain e l'uso della macro di LOG per la traccia). Individuare il nome usato da MSP per la registrazione per la traccia. si tratta in genere del nome della DLL. viene indicato di seguito come " &lt; nome dll &gt; ". Per abilitare la traccia, utilizzare un editor del registro di sistema ("Regedit.exe" o "Regedt32.exe") per individuare la chiave "HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Tracing" ed eseguire le operazioni seguenti. Si noti che tutti i valori indicati di seguito, ad eccezione del valore EnableDebuggerTracing, devono essere creati automaticamente dopo aver eseguito l'MSP per la prima volta.

-   Per abilitare la traccia nei debugger in modalità utente e kernel, impostare il valore **DWORD** <dll name> \\ EnableDebuggerTracing su 1. Facoltativamente, usare il  valore DWORD <dll name> \\ ConsoleTracing mask per abilitare o disabilitare diversi livelli di output di traccia. il valore predefinito è 0xFFFF0000, che Abilita tutti i livelli di traccia.
-   Per abilitare la traccia in un file, impostare il valore **DWORD** <dll name> \\ EnableFileTracing su 1. Facoltativamente, utilizzare il valore di stringa <dll name> \\ FileDirectory per modificare il percorso del file di log. Facoltativamente, usare il  valore DWORD <dll name> \\ FileTracingMask per abilitare o disabilitare diversi livelli di output di traccia (il valore predefinito è 0xFFFF0000, che Abilita tutti i livelli di traccia).
-   Per abilitare la traccia in una finestra della console separata, separata dalla DLL, impostare il valore **DWORD** EnableConsoleTracing su 1 e impostare anche il valore **DWORD** <dll name> \\ EnableConsoleTracing su 1. Facoltativamente, usare il  valore DWORD <dll name> \\ ConsoleTracing mask per abilitare o disabilitare diversi livelli di output di traccia. il valore predefinito è 0xFFFF0000, che Abilita tutti i livelli di traccia.

 

 



