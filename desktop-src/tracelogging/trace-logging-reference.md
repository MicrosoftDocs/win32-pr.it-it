---
title: Informazioni di riferimento su TraceLogging
description: Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa. TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6563186411ace599f249220b9fd44b9ee4c682fdebd1391b4a3027a87c3482e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349991"
---
# <a name="tracelogging-reference"></a>Informazioni di riferimento su TraceLogging

Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa.

TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice. TraceLogging consente di includere dati strutturati con eventi, correlare eventi e non richiede un file XML manifesto di strumentazione separato.

<span class="underline">Per sviluppatori WinRT</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) è stato esteso in Windows 10 per registrare eventi ETW (Event Tracing for Windows) autodescritti senza la necessità di un manifesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che forniscono il controllo sul formato e sul contenuto degli eventi Start e Stop. Inoltre, le attività possono essere annidate.

<span class="underline">Per sviluppatori di codice gestito (Microsoft .NET Framework)</span>

-   La [classe EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornita con le versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto. Tuttavia, agli sviluppatori era necessario usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano trasformati automaticamente in un manifesto ETW. A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare Direttamente EventSource per registrare eventi autodescrittori che non richiedono un manifesto.

<span class="underline">Per sviluppatori C/C++</span>

-   TraceLoggingProvider.h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel. Questa API non è adatta per l'uso in scenari dinamici (con script), ad esempio Javascript. I collegamenti seguenti descrivono l'API C/C++.

<!-- -->

-   [Classi](trace-logging-classes.md)
-   [Funzioni](trace-logging-functions.md)
-   [Macro](trace-logging-macros.md)

Si noti che il valore di WINVER influisce sul comportamento di TraceLoggingProvider.h.

-   Se WINVER non viene impostato prima di includere <windows.h>, <windows.h> imposta WINVER su un valore predefinito corrispondente alla versione dell'SDK.
-   Usando TraceLoggingProvider.h con WINVER impostato su 0x0602 (Windows 8) o versione successiva, il programma non verrà eseguito in Windows Vista o Windows 7.
-   Usando TraceLoggingProvider.h con WINVER impostato su 0x0600 (Windows Vista) o 0x0601 (Windows 7), il programma verrà configurato per la compatibilità e funzionerà sulle versioni specificate di Windows.

 

 