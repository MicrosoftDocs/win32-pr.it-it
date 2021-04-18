---
description: Traccia Winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306876"
---
# <a name="winsock-tracing"></a>Traccia Winsock

## <a name="introduction"></a>Introduzione

La traccia Winsock è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari finali per tracciare alcuni eventi socket di Windows con un sovraccarico minimo. L'obiettivo di aggiungere la traccia al dettaglio a Windows Sockets è quello di consentire migliori funzionalità di diagnostica per gli sviluppatori e il supporto del prodotto. La traccia eventi di rete Winsock supporta la traccia di operazioni socket per le applicazioni IPv4 e IPv6. La traccia delle modifiche del catalogo Winsock supporta la traccia delle modifiche apportate al catalogo Winsock dai provider di servizi a più livelli (LSP). La traccia Winsock è supportata in Windows Vista e versioni successive.

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

Quando si verifica un errore imprevisto in un socket, l'indizio principale per diagnosticare il problema è il codice di errore restituito. Molto spesso, il codice di errore restituito non spiega perché si è verificato l'errore, soprattutto quando l'errore viene avviato dal trasporto di rete sottostante. La traccia Winsock fornisce un livello di traccia più dettagliato che consente di registrare informazioni aggiuntive per rilevare il danneggiamento del buffer e le applicazioni scritte in modo non corretto.

La traccia Winsock utilizza Event Tracing for Windows (ETW), una funzionalità di traccia a utilizzo generale e ad alta velocità fornita dal sistema operativo. Utilizzando un meccanismo di memorizzazione nel buffer e di registrazione implementato nel kernel, ETW fornisce un meccanismo di traccia per gli eventi generati da applicazioni in modalità utente e driver di dispositivo in modalità kernel. Inoltre, ETW offre la possibilità di abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate in ambienti di produzione senza richiedere riavvii o riavvii di applicazioni. Il meccanismo di registrazione utilizza buffer che vengono scritti su disco da un thread del writer asincrono. Questo consente alle applicazioni server su larga scala di scrivere eventi con un disturbo minimo. ETW è stato introdotto per la prima volta in Windows 2000. Il supporto per la traccia Winsock mediante ETW è stato aggiunto in Windows Vista e versioni successive. Per informazioni generali su ETW, vedere [migliorare il debug e l'ottimizzazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

La traccia Winsock può essere abilitata solo a livello di sistema operativo per tutti i processi e i thread in esecuzione in un computer. Attualmente non è possibile abilitare la traccia Winsock solo per un singolo processo o thread. Quando la traccia degli eventi di rete Winsock è abilitata, vengono tracciate tutte le applicazioni socket (sia IPv4 che IPv6) in un computer.

Gli argomenti seguenti descrivono la traccia Winsock in modo più dettagliato:

-   [Livelli di traccia Winsock](winsock-tracing-levels.md)
-   [Controllo della traccia Winsock](control-of-winsock-tracing.md)
-   [Dettagli traccia eventi di rete Winsock](winsock-tracing-event-details.md)
-   [Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Migliorare il debug e la regolazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Funzionalità di debug e di traccia](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
