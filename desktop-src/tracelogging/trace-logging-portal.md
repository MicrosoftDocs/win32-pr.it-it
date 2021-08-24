---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1263f040707a1e0ea7578b35165c581f6847b5263af42dff76808a7518e5fcae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818511"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Scopo

TraceLogging è il nuovo framework Windows 10 di traccia eventi per le applicazioni in modalità utente e i driver in modalità kernel. TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.

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
<td>TraceLogging è la nuova traccia Windows 10 eventi per le applicazioni in modalità utente e i driver in modalità kernel. TraceLogging è un formato per l'autodescrittura di Event Tracing for Windows (ETW). TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Uso di TraceLogging</a><br/></td>
<td>Negli argomenti seguenti viene fornito un avvio rapido di TraceLogging per il codice nativo e gestito, con esempi.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">Informazioni di riferimento su TraceLogging</a><br/></td>
<td>Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa.<br/> TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice. TraceLogging consente di includere dati strutturati con eventi, correlare eventi e non richiede un file XML manifesto di strumentazione separato.<br/> <span class="underline">Per sviluppatori WinRT</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> è stato esteso in Windows 10 per registrare eventi ETW (Event Tracing for Windows) autodescritti senza la necessità di un manifesto.</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> è stato esteso in Windows 10 per fornire metodi di avvio e arresto dell'attività che forniscono il controllo sul formato e sul contenuto degli eventi Start e Stop. Inoltre, le attività possono essere annidate.</li>
</ul>
<span class="underline">Per sviluppatori di codice gestito (Microsoft .NET Framework)</span><br/>
<ul>
<li>La <a href="/dotnet/api/system.diagnostics.tracing.eventsource">classe EventSource</a> fornita con le versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto. Tuttavia, agli sviluppatori era necessario usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano trasformati automaticamente in un manifesto ETW. A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare Direttamente EventSource per registrare eventi autodescrittori che non richiedono un manifesto.</li>
</ul>
<span class="underline">Per sviluppatori C/C++</span><br/>
<ul>
<li>TraceLoggingProvider.h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel. Questa API non è adatta per l'uso in scenari dinamici (con script), ad esempio Javascript. I collegamenti seguenti descrivono l'API C/C++.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Sviluppatori

TraceLogging è progettato per l'uso da parte degli sviluppatori di applicazioni in modalità utente e degli sviluppatori di driver in modalità kernel che vogliono aggiungere la traccia al codice.

