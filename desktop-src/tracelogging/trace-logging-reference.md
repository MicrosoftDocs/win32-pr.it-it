---
title: Riferimento a TraceLogging
description: Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa. TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399647"
---
# <a name="tracelogging-reference"></a>Riferimento a TraceLogging

Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa.

TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice. TraceLogging consente di includere dati strutturati con eventi, correlare gli eventi e non richiede un file XML del manifesto di strumentazione separato.

<span class="underline">Per gli sviluppatori WinRT</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) è stato esteso in Windows 10 per registrare eventi ETW (descrittivi Event Tracing for Windows) senza la necessità di un manifesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che consentono di controllare il formato e il contenuto degli eventi di avvio e arresto. Inoltre, le attività possono essere nidificate.

<span class="underline">Per gli sviluppatori di codice gestito (Microsoft .NET Framework)</span>

-   La classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornita con versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto. Tuttavia, gli sviluppatori dovevano usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano automaticamente convertiti in un manifesto ETW. A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare EventSource direttamente per registrare eventi autodescrittivi che non richiedono un manifesto.

<span class="underline">Per gli sviluppatori C/C++</span>

-   TraceLoggingProvider. h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel. Questa API non è particolarmente adatta per l'uso in scenari dinamici (con script), ad esempio JavaScript. I collegamenti seguenti descrivono l'API C/C++.

<!-- -->

-   [Classi](trace-logging-classes.md)
-   [Funzioni](trace-logging-functions.md)
-   [Macro](trace-logging-macros.md)

Si noti che il valore di WINVER influirà sul comportamento di TraceLoggingProvider. h.

-   Se WINVER non è impostato prima di includere <> Windows. h, <Windows. h> imposterà WINVER su un valore predefinito corrispondente alla versione dell'SDK.
-   Se si utilizza TraceLoggingProvider. h con WINVER impostato su 0x0602 (Windows 8) o versione successiva, il programma non viene eseguito in Windows Vista o Windows 7.
-   Se si utilizza TraceLoggingProvider. h con WINVER impostato su 0x0600 (Windows Vista) o 0x0601 (Windows 7), il programma verrà configurato per la compatibilità e funzionerà nelle versioni di Windows specificate.

 

 