---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103733647"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Scopo

TraceLogging è il nuovo Framework di analisi degli eventi di Windows 10 per le applicazioni in modalità utente e i driver in modalità kernel. TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="trace-logging-about.md">Informazioni su TraceLogging</a><br/></td>
<td>TraceLogging è la nuova traccia eventi di Windows 10 per le applicazioni in modalità utente e i driver in modalità kernel. TraceLogging è un formato per il Event Tracing for Windows (ETW) autodescrittivo. TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Uso di TraceLogging</a><br/></td>
<td>Gli argomenti seguenti forniscono una guida introduttiva a TraceLogging per il codice nativo e gestito, con esempi.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">Riferimento a TraceLogging</a><br/></td>
<td>Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa.<br/> TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice. TraceLogging consente di includere dati strutturati con eventi, correlare gli eventi e non richiede un file XML del manifesto di strumentazione separato.<br/> <span class="underline">Per gli sviluppatori WinRT</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> è stato esteso in Windows 10 per registrare eventi ETW (descrittivi Event Tracing for Windows) senza la necessità di un manifesto.</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che consentono di controllare il formato e il contenuto degli eventi di avvio e arresto. Inoltre, le attività possono essere nidificate.</li>
</ul>
<span class="underline">Per gli sviluppatori di codice gestito (Microsoft .NET Framework)</span><br/>
<ul>
<li>La classe <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> fornita con versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto. Tuttavia, gli sviluppatori dovevano usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano automaticamente convertiti in un manifesto ETW. A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare EventSource direttamente per registrare eventi autodescrittivi che non richiedono un manifesto.</li>
</ul>
<span class="underline">Per gli sviluppatori C/C++</span><br/>
<ul>
<li>TraceLoggingProvider. h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel. Questa API non è particolarmente adatta per l'uso in scenari dinamici (con script), ad esempio JavaScript. I collegamenti seguenti descrivono l'API C/C++.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Sviluppatori

TraceLogging è progettato per essere utilizzato dagli sviluppatori di applicazioni in modalità utente e dagli sviluppatori di driver in modalità kernel che desiderano aggiungere la traccia al codice.

