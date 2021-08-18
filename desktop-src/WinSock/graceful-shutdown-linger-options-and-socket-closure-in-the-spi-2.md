---
description: È importante distinguere tra l'arresto di una connessione socket e la chiusura di un socket.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Arresto normale, opzioni residue e chiusura socket in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5791732404948fe59d3f5c15c2ac46cdbba8d8327fb3dc5f794be1f070a9eeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132134"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Arresto normale, opzioni residue e chiusura socket in SPI

È importante distinguere tra l'arresto di una connessione socket e la chiusura di un socket. L'arresto di una connessione socket comporta uno scambio di messaggi di protocollo tra i due endpoint, che successivamente viene definito sequenza di arresto. Vengono definite due classi generali di sequenze di arresto: normale e abortiva. In una sequenza di arresto normale, tutti i dati che sono stati accodati ma non ancora trasmessi possono essere inviati prima della chiusura della connessione. In un arresto interrotto, tutti i dati non invii vengono persi. L'occorrenza di una sequenza di arresto (normale o abortiva) può essere usata anche per fornire un'indicazione FD CLOSE alle applicazioni associate che indicano che è in corso \_ un arresto. Se invece si chiude un socket, l'handle del socket viene deallocato in modo che l'applicazione non possa più fare riferimento al socket o usarlo in alcun modo.

Nei socket Windows è possibile usare sia la funzione [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) che la funzione [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) per avviare una sequenza di arresto, mentre la funzione [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) viene usata per deallocare gli handle di socket e liberare le risorse associate. Tuttavia, una certa confusione deriva dal fatto che la funzione **WSPCloseSocket** causerà in modo implicito una sequenza di arresto se non si è già verificata. In realtà, è diventato una pratica di programmazione piuttosto comune basarsi su questa funzionalità e usare **WSPCloseSocket** per avviare la sequenza di arresto e deallocare l'handle del socket.

Per semplificare questo utilizzo, l'interfaccia socket fornisce controlli tramite il meccanismo delle opzioni socket che consente al programmatore di indicare se la sequenza di arresto implicita deve essere normale o abortiva e anche se la funzione deve essere residua, non completa immediatamente, per consentire il completamento di una sequenza di arresto normale.

Stabilendo i valori appropriati per le opzioni di socket SO LINGER e SO DONTLINGER, è possibile ottenere i tipi di comportamento seguenti con la \_ \_ funzione [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))

-   Sequenza di arresto abortiva, restituzione immediata [**da WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))
-   Arresto normale, restituzione ritardata fino al completamento della sequenza di arresto o alla scadenza di un intervallo di tempo specificato. Se l'intervallo di tempo scade prima del completamento della sequenza di arresto normale, viene eseguita una sequenza di arresto abortiva e viene restituito [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))
-   Arresto normale, restituzione immediata e completamento della sequenza di arresto in background. Comportamento predefinito. Si noti, tuttavia, che l'applicazione non ha modo di sapere quando (o se) la sequenza di arresto normale viene completata.

Una tecnica che può essere usata per ridurre al minimo le probabilità che si verifichino problemi durante la chiusura della connessione consiste nel non basarsi su un arresto implicito avviato da [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) Viene invece usata una delle due funzioni di arresto esplicite ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPSendDisconnect).**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) A sua volta, l'applicazione peer riceverà un'indicazione FD CLOSE che indica che sono stati ricevuti tutti i \_ dati in sospeso. A tale scopo, nella tabella seguente vengono illustrate le funzioni che verrebbero richiamate dai componenti client e server di un'applicazione, in cui il client è responsabile dell'avvio di un arresto normale.

| Lato client                                                                                                                         | Sul lato server                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) Richiama [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD SEND) per segnalare la fine della sessione e che il client non dispone \_ di altri dati da inviare. |                                                                                                              |
|                                                                                                                                     | (2) Riceve FD CLOSE, che indica l'arresto normale \_ in corso e che tutti i dati sono stati ricevuti.        |
|                                                                                                                                     | (3) Invia tutti i dati di risposta rimanenti.                                                                       |
| (5') Ottiene FD \_ READ e richiama recv per ottenere i dati di risposta inviati dal server.                                                         | (4) Richiama [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD SEND) per indicare che il server non \_ ha più dati da inviare. |
| (5) Riceve l'indicazione FD \_ CLOSE.                                                                                                  | (4') Richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) Richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

La sequenza temporale viene mantenuta dal passaggio (1) al passaggio (6) tra il client e il server, ad eccezione dei passaggi (4') e (5') che hanno solo un significato di temporizzazione locale nel senso che il passaggio (5) segue il passaggio (5') sul lato client mentre il passaggio (4') segue il passaggio (4) sul lato server, senza alcuna relazione di temporizzazione con l'entità remota.

 

 
