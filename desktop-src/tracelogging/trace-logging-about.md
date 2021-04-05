---
title: Informazioni su TraceLogging
description: TraceLogging è la nuova traccia eventi di Windows 10 per le applicazioni in modalità utente e i driver in modalità kernel.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872641"
---
# <a name="about-tracelogging"></a>Informazioni su TraceLogging

TraceLogging è la nuova traccia eventi di Windows 10 per le applicazioni in modalità utente e i driver in modalità kernel. TraceLogging è un formato per il Event Tracing for Windows (ETW) autodescrittivo. TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.

TraceLogging offre la semplicità di Windows software Trace Preprocessor (WPP) con il vantaggio aggiuntivo di poter includere dati strutturati con eventi, la possibilità di correlare gli eventi e tutto senza richiedere un file XML manifesto di strumentazione separato. Gli eventi sono autodescrittivi, il che significa che non è necessario che un file binario contenente il manifesto di strumentazione venga registrato nel sistema per poter usare le API TDH (Trace Data Helper) per decodificare e visualizzare gli eventi.

Event Tracing for Windows (ETW) è stato introdotto con Windows 2000 e aggiornato in Windows Vista. Tracelogging si basa sulle API ETW di Windows Vista. I provider possono utilizzare la tecnologia TraceLogging e continuare a lavorare in Windows Vista. I controller esistenti (con Windows VistaAPIs) possono essere usati per controllare i provider TraceLogging.

TraceLogging è compatibile anche con gli strumenti esistenti. I provider che utilizzano ETW basato su manifesto sono ancora supportati. Non è necessario convertire i provider ETW basati su manifesti nei provider TraceLogging, a meno che non si voglia sfruttare la semplicità fornita da TraceLogging. Anche la traccia WPP è ancora supportata.

TraceLogging si basa su ETW, ma introduce diversi miglioramenti importanti:

-   La traccia di un evento è semplice come una chiamata API.
-   Gli eventi sono autodescrittivi e non richiedono file binari aggiuntivi contenenti il manifesto dell'evento compilato per interpretare l'evento. Tutti i metadati relativi all'evento vengono registrati nell'evento.
-   Le attività all'interno di un singolo processo possono essere facilmente espresse tramite eventi di avvio e interruzione.
-   TraceLogging è compatibile con il supporto strumentazione esistente. Le nuove API ETW continuano a supportare i vecchi provider. È possibile investire nelle nuove API ETW per scenari strategici lasciando i vecchi punti di strumentazione così come sono.
-   TraceLogging offre la stessa API di traccia eventi per Windows 10, Xbox One e Windows 10 Mobile.
-   Le API TraceLogging sono accessibili da C, C++, .NET e Windows Runtime.

## <a name="api-high-level-overview"></a>Panoramica dell'API di alto livello

Sono disponibili tre API TraceLogging separate destinate a diversi destinatari di sviluppatori. Ogni API è stata progettata per soddisfare diversi set di requisiti, in base alle esigenze dei destinatari di tale API.

Per gli sviluppatori WinRT:

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) è stato esteso in Windows 10 per registrare eventi ETW (descrittivi Event Tracing for Windows) senza la necessità di un manifesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che consentono di controllare il formato e il contenuto degli eventi di avvio e arresto. Inoltre, le attività possono essere nidificate.

Per gli sviluppatori C/C++:

-   TraceLoggingProvider. h contiene l'API più efficiente, tuttavia questa API non è particolarmente adatta per l'uso in scenari dinamici (con script), ad esempio JavaScript. Questa API può essere usata in modalità utente e codice in modalità kernel.

Per gli sviluppatori di codice gestito (Microsoft .NET Framework):

-   La classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornita con le versioni precedenti del .NET Framework già supportata la scrittura di eventi ETW, generando automaticamente il manifesto e incorporando il manifesto nel flusso di eventi. Tuttavia, lo sviluppatore deve comunque tenere traccia del manifesto per decodificare gli eventi, a meno che non si lavori in uno scenario in cui il manifesto incorporato era supportato. TraceLogging consente di eliminare completamente il manifesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla traccia eventi](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 