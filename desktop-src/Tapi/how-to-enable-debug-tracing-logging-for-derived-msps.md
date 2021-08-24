---
description: La procedura seguente descrive come abilitare la traccia e la registrazione di debug.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Come abilitare la traccia/registrazione del debug per msps derivati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565b66055a43edbe7556e640f8e368aab84fab206bced431c22578a7e21a94ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140524"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Come abilitare la traccia/registrazione del debug per msps derivati

Assicurarsi prima di tutto che l'implementazione del file MSP derivato abbia seguito le linee guida della sezione precedente per quanto riguarda la traccia di debug (definizione del simbolo del preprocessore MSPLOG, registrazione per la traccia durante DllMain e uso della macro LOG per la traccia). Individuare il nome utilizzato dall'msp durante la registrazione per la traccia(in genere deve essere il nome della DLL, come indicato di seguito come " &lt; nome dll &gt; "). Per abilitare la traccia, usare un editor del Registro di sistema ("Regedit.exe" o "Regedt32.exe") per individuare la chiave "HKEY LOCAL MACHINE Software Microsoft Tracing" ed \_ eseguire le operazioni \_ \\ \\ \\ seguenti. Si noti che tutti i valori indicati di seguito, ad eccezione del valore EnableDebuggerTracing, devono essere creati automaticamente dopo la prima esecuzione di MSP.

-   Per abilitare la traccia ai debugger in modalità utente e kernel, impostare il **valore DWORD** <dll name> \\ EnableDebuggerTracing su 1. Facoltativamente, usare il **valore DWORD** <dll name> ConsoleTracing Mask per abilitare o disabilitare vari livelli di output di traccia (il valore predefinito è 0xFFFF0000, che abilita tutti i livelli \\ di traccia).
-   Per abilitare la traccia in un file, impostare il **valore DWORD** <dll name> \\ EnableFileTracing su 1. Facoltativamente, usare il valore stringa <dll name> \\ FileDirectory per modificare il percorso del file di log. Facoltativamente, usare il **valore DWORD** <dll name> FileTracingMask per abilitare o disabilitare vari livelli di output di traccia (il valore predefinito è 0xFFFF0000, che abilita tutti i livelli \\ di traccia).
-   Per abilitare la traccia in una finestra della console separata, separata da DLL, impostare il valore **DWORD** EnableConsoleTracing su 1 e anche impostare il **valore DWORD** <dll name> \\ EnableConsoleTracing su 1. Facoltativamente, usare il **valore DWORD** <dll name> ConsoleTracing Mask per abilitare o disabilitare vari livelli di output di traccia (il valore predefinito è 0xFFFF0000, che abilita tutti i livelli \\ di traccia).

 

 



