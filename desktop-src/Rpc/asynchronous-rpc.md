---
title: RPC asincrona
description: La chiamata RPC (Remote Procedure Call) asincrona è un'estensione Microsoft che risolve diverse limitazioni del modello RPC tradizionale come definito da Open Software Foundation \ 8211; Distributed Computing Environment (OSF-DCE).
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- RPC (Remote Procedure Call) RPC, descritta, RPC asincrona
- RPC asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ac79a30fd01aeba1efb3cbd2b7cc741f26238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118238"
---
# <a name="asynchronous-rpc"></a>RPC asincrona

La chiamata RPC (Remote Procedure Call) asincrona è un'estensione Microsoft che risolve diverse limitazioni del modello RPC tradizionale come definito da Open Software Foundation-Distributed Computing Environment (OSF-DCE). RPC asincrona separa una chiamata di procedura remota dal relativo valore restituito, che risolve le seguenti limitazioni di RPC tradizionale e sincrona:

-   **Più chiamate in attesa da un client a thread singolo.** Nel modello RPC tradizionale un client viene bloccato in una chiamata di procedura remota finché la chiamata non restituisce. In questo modo si impedisce a un client di avere più chiamate in attesa, mantenendo comunque il thread disponibile per eseguire altre operazioni.
-   **Client lenti o ritardati.** Un client lento per produrre dati potrebbe voler eseguire una chiamata di procedura remota con dati iniziali e quindi fornire dati aggiuntivi quando vengono prodotti. Questa operazione non è possibile con RPC convenzionali (sincrona).
-   **Server lenti o ritardati.** Una chiamata di procedura remota che richiede molto tempo per il completamento collegherà il thread di invio per la durata dell'attività. Con RPC asincrono, il server può avviare un'operazione separata (asincrona) per elaborare la richiesta e restituire la risposta quando è disponibile. Il server può anche inviare la risposta in modo incrementale quando i risultati diventano disponibili senza dover bloccare un thread di invio per la durata della chiamata remota. Rendendo asincrona l'applicazione client, è possibile impedire a un server lento di vincolare inutilmente un'applicazione client.
-   **Trasferimento di grandi quantità di dati.** Il trasferimento di grandi quantità di dati tra il client e il server, in particolare sui collegamenti lenti, collega sia il thread del client che il thread di Server Manager per la durata del trasferimento. Con RPC e pipe asincrone, il trasferimento dei dati può avvenire in modo incrementale e senza impedire al client o al server di eseguire altre attività.

Si sfruttano i meccanismi RPC asincroni dichiarando funzioni con l' \[ attributo [**Async**](/windows/desktop/Midl/async) \] . Poiché si esegue questa dichiarazione in un file di configurazione degli attributi (ACF), non è necessario apportare alcuna modifica al file IDL (Interface Definition Language). il protocollo RPC asincrono non ha alcun effetto sul protocollo wire (modalità di trasmissione dei dati tra client e server). Ciò significa che i client sincroni e asincroni possono comunicare con un'applicazione server asincrona.

In questa sezione viene presentata una panoramica sullo sviluppo di applicazioni distribuite mediante RPC asincrono. La panoramica è illustrata nelle sezioni seguenti:

-   [Dichiarazione di funzioni asincrone](declaring-asynchronous-functions.md)
-   [RPC asincrona lato client](client-side-asynchronous-rpc.md)
-   [RPC asincrona sul lato server](server-side-asynchronous-rpc.md)
-   [Ordinamento causale di chiamate asincrone](causal-ordering-of-asynchronous-calls.md)
-   [Gestione degli errori](error-handling.md)
-   [RPC asincrona sul protocollo named pipe](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Uso di RPC asincrone con pipe DCE](using-asynchronous-rpc-with-dce-pipes.md)
-   [DCOM asincrono](asynchronous-dcom.md)

 

 