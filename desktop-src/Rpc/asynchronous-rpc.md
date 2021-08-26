---
title: RPC asincrona
description: RPC (Asynchronous Remote Procedure Call) è un'estensione Microsoft che risolve diverse limitazioni del modello RPC tradizionale, come definito da Open Software Foundation \ 8211;Distributed Computing Environment (OSF-DCE).
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- RPC Remote Procedure Call, descritto, RPC asincrono
- RPC asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4a5f160054f78f0a5737993d1a030957af930ab036e73dbcea0a039125964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023541"
---
# <a name="asynchronous-rpc"></a>RPC asincrona

RPC (Asynchronous Remote Procedure Call) è un'estensione Microsoft che risolve diverse limitazioni del modello RPC tradizionale definito da Open Software Foundation–Distributed Computing Environment (OSF-DCE). Rpc asincrona separa una chiamata di procedura remota dal relativo valore restituito, risolvendo le limitazioni seguenti della RPC tradizionale sincrona:

-   **Più chiamate in sospeso da un client a thread singolo.** Nel modello RPC tradizionale, un client viene bloccato in una chiamata di procedura remota finché la chiamata non viene restituita. In questo modo si impedisce a un client di avere più chiamate in sospeso, mantenendo comunque il thread disponibile per eseguire altre operazioni.
-   **Client lenti o ritardati.** Un client lento a produrre dati potrebbe voler effettuare una chiamata di procedura remota con i dati iniziali e quindi fornire dati aggiuntivi durante la produzione. Ciò non è possibile con rpc convenzionale (sincrona).
-   **Server lenti o ritardati.** Una chiamata di procedura remota che richiede molto tempo per il completamento consente di collegare il thread di invio per la durata dell'attività. Con rpc asincrono, il server può avviare un'operazione separata (asincrona) per elaborare la richiesta e inviare nuovamente la risposta quando è disponibile. Il server può anche inviare la risposta in modo incrementale non appena i risultati diventano disponibili senza dover associare un thread di invio per la durata della chiamata remota. Rendendo asincrona l'applicazione client, è possibile impedire a un server lento di creare inutilmente un'applicazione client.
-   **Trasferimento di grandi quantità di dati.** Il trasferimento di grandi quantità di dati tra il client e il server, in particolare su collegamenti lenti, collega sia il thread client che il thread di server manager per la durata del trasferimento. Con RPC e pipe asincrone, il trasferimento dei dati può essere eseguito in modo incrementale e senza bloccare l'esecuzione di altre attività da parte del client o del server.

È possibile sfruttare i meccanismi RPC asincroni dichiarando le funzioni con \[ [**l'attributo async.**](/windows/desktop/Midl/async) \] Poiché questa dichiarazione viene apportata in un file di configurazione degli attributi (ACF), non è necessario apportare modifiche al file IDL (Interface Definition Language). RPC asincrona non ha alcun effetto sul protocollo di trasmissione (modalità di trasmissione dei dati tra client e server). Ciò significa che i client sincroni e asincroni possono comunicare con un'applicazione server asincrona.

Questa sezione presenta una panoramica dello sviluppo di applicazioni distribuite tramite RPC asincrono. La panoramica viene presentata nelle sezioni seguenti:

-   [Dichiarazione di funzioni asincrone](declaring-asynchronous-functions.md)
-   [RPC asincrona lato client](client-side-asynchronous-rpc.md)
-   [RPC asincrona lato server](server-side-asynchronous-rpc.md)
-   [Ordinamento causale delle chiamate asincrone](causal-ordering-of-asynchronous-calls.md)
-   [Gestione degli errori](error-handling.md)
-   [RPC asincrona sul protocollo Named Pipe](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Uso di RPC asincrono con pipe DCE](using-asynchronous-rpc-with-dce-pipes.md)
-   [DCOM asincrono](asynchronous-dcom.md)

 

 