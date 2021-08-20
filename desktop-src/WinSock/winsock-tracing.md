---
description: Traccia winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Traccia winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2d9593f4c2cea47e722075f1611151fb276cdf2646a2c9898a9c8d7d156098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321671"
---
# <a name="winsock-tracing"></a>Traccia winsock

## <a name="introduction"></a>Introduzione

La traccia Winsock è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari per la vendita al dettaglio per tracciare determinati eventi Windows socket con sovraccarico minimo. L'obiettivo dell'aggiunta della traccia al dettaglio Windows Sockets è quello di consentire funzionalità di diagnostica migliori per gli sviluppatori e il supporto tecnico del prodotto. La traccia eventi di rete Winsock supporta operazioni socket di traccia per applicazioni IPv4 e IPv6. La traccia delle modifiche del catalogo Winsock supporta la traccia delle modifiche apportate al catalogo Winsock da provider di servizi su più livelli(LSP). La traccia Winsock è supportata in Windows Vista e versioni successive.

> [!Note]  
> I provider di servizi su più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

 

Quando si verifica un errore imprevisto in un socket, l'indicazione principale per diagnosticare il problema è il codice di errore restituito. Molto spesso, il codice di errore restituito non spiega il motivo per cui si è verificato l'errore, soprattutto quando l'errore viene avviato dal trasporto di rete sottostante. La traccia winsock offre un livello di traccia più dettagliato che consente di registrare informazioni aggiuntive per rilevare il danneggiamento del buffer e le applicazioni scritte in modo non valido.

La traccia Winsock usa Event Tracing for Windows (ETW), una funzionalità di traccia ad alta velocità per utilizzo generico fornita dal sistema operativo. Usando un meccanismo di memorizzazione nel buffer e registrazione implementato nel kernel, ETW fornisce un meccanismo di traccia per gli eventi generati dalle applicazioni in modalità utente e dai driver di dispositivo in modalità kernel. Inoltre, ETW offre la possibilità di abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii dell'applicazione. Il meccanismo di registrazione usa buffer scritti su disco da un thread writer asincrono. Ciò consente alle applicazioni server su larga scala di scrivere eventi con un numero minimo di eventi. ETW è stato introdotto per la Windows 2000. Il supporto per la traccia Winsock tramite ETW è stato aggiunto in Windows Vista e versioni successive. Per informazioni generali su ETW, vedere [Migliorare il debug e l'ottimizzazione delle prestazioni con ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

La traccia Winsock può essere abilitata solo a livello di sistema operativo per tutti i processi e i thread in esecuzione in un computer. La traccia Winsock non può attualmente essere abilitata solo per un singolo processo o thread. Quando la traccia degli eventi di rete Winsock è abilitata, vengono tracciate tutte le applicazioni socket (sia IPv4 che IPv6) in un computer.

Gli argomenti seguenti descrivono la traccia winsock in modo più dettagliato:

-   [Livelli di traccia di Winsock](winsock-tracing-levels.md)
-   [Controllo della traccia winsock](control-of-winsock-tracing.md)
-   [Dettagli di Traccia eventi di rete Winsock](winsock-tracing-event-details.md)
-   [Dettagli traccia modifiche catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Migliorare il debug e la regolazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Funzionalità di debug e traccia](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
