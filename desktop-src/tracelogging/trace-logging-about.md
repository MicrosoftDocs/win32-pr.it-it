---
title: Informazioni su TraceLogging
description: TraceLogging è il nuovo Windows 10 traccia eventi per le applicazioni in modalità utente e i driver in modalità kernel.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cc38210bf4c3ed1ed0b1ebf56ca22a0597b9288fc30ae4c0231d5317465644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218392"
---
# <a name="about-tracelogging"></a>Informazioni su TraceLogging

TraceLogging è il nuovo Windows 10 traccia eventi per le applicazioni in modalità utente e i driver in modalità kernel. TraceLogging è un formato per la descrizione autodescrittura di Event Tracing for Windows (ETW). TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.

TraceLogging offre la semplicità del preprocessore WPP (Software Trace Preprocessor) di Windows con il vantaggio aggiuntivo di poter includere dati strutturati con eventi, la possibilità di correlare gli eventi e tutto senza richiedere un file XML del manifesto della strumentazione separato. Gli eventi sono autodescrittori, ovvero non è necessario registrare nel sistema un file binario contenente il manifesto di strumentazione per poter usare le API TDH (Trace Data Helper) per decodificare e visualizzare gli eventi.

Event Tracing for Windows (ETW) è stato introdotto con Windows 2000 e aggiornato in Windows Vista. Il tracelogging si basa sulle API ETW Windows Vista. I provider possono usare la tecnologia TraceLogging e lavorare ancora Windows Vista. È possibile usare controller esistenti Windows VistaAPIs per controllare i provider TraceLogging.

TraceLogging è compatibile anche con gli strumenti esistenti. I provider che usano ETW basato su manifesto sono ancora supportati. Non è necessario convertire i provider ETW basati su manifesto in provider TraceLogging a meno che non si voglia sfruttare la semplicità fornita da TraceLogging. Anche la traccia WPP è ancora supportata.

TraceLogging si basa su ETW, ma introduce diversi importanti miglioramenti:

-   La traccia di un evento è semplice quanto una chiamata API.
-   Gli eventi sono autodescritti e non richiedono file binari aggiuntivi contenenti il manifesto dell'evento compilato per interpretare l'evento. Tutti i metadati relativi all'evento vengono registrati nell'evento.
-   Le attività all'interno di un singolo processo possono essere espresse facilmente tramite eventi di avvio e arresto.
-   TraceLogging è compatibile con il supporto di strumentazione esistente. Le nuove API ETW continuano a supportare i provider vecchi. È possibile investire nelle nuove API ETW per scenari strategici lasciando i punti di strumentazione non più disponibili.
-   TraceLogging offre la stessa API di traccia eventi per Windows 10, Xbox One e Windows 10 Mobile.
-   Le API TraceLogging sono accessibili da C, C++, .NET e Windows Runtime.

## <a name="api-high-level-overview"></a>Panoramica generale dell'API

Sono disponibili tre API TraceLogging separate per diversi destinatari di sviluppatori. Ogni API è stata progettata per soddisfare diversi set di requisiti in base alle esigenze dei destinatari di tale API.

Per gli sviluppatori WinRT:

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) è stato esteso in Windows 10 per registrare eventi ETW (Event Tracing for Windows) autodescritti senza la necessità di un manifesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che forniscono il controllo sul formato e sul contenuto degli eventi Start e Stop. Inoltre, le attività possono essere annidate.

Per gli sviluppatori C/C++:

-   TraceLoggingProvider.h contiene l'API più efficiente, tuttavia questa API non è adatta per l'uso in scenari dinamici (con script), ad esempio Javascript. Questa API può essere usata nel codice in modalità utente e in modalità kernel.

Per gli sviluppatori di codice gestito (Microsoft .NET Framework):

-   La [classe EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornita con le versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW, generando automaticamente il manifesto e incorporando il manifesto nel flusso di eventi. Tuttavia, lo sviluppatore doveva comunque tenere traccia del manifesto per decodificare gli eventi , a meno che non si lavora in uno scenario in cui il manifesto incorporato fosse supportato. TraceLogging consente di eliminare completamente il manifesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Event Tracing](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 