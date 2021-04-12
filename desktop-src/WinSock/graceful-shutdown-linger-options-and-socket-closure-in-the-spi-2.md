---
description: È importante distinguere tra l'arresto di una connessione socket e la chiusura di un socket.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Arresto normale, opzioni Linger e chiusura del socket in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743cae48977421c08611c79053520799420e9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526166"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Arresto normale, opzioni Linger e chiusura del socket in SPI

È importante distinguere tra l'arresto di una connessione socket e la chiusura di un socket. L'arresto di una connessione socket comporta uno scambio di messaggi di protocollo tra i due endpoint, che in seguito viene indicato come sequenza di arresto. Sono definite due classi generali di sequenze di arresto: aggraziate e interrotte. In una sequenza di arresto normale, tutti i dati che sono stati accodati ma non ancora trasmessi possono essere inviati prima della chiusura della connessione. In caso di arresto anomalo, tutti i dati non inviati andranno perduti. L'occorrenza di una sequenza di arresto (normale o abortica) può essere usata anche per fornire un' \_ indicazione di chiusura FD alle applicazioni associate, a indicare che è in corso un arresto. La chiusura di un socket, d'altra parte, causa la deallocazione dell'handle del socket, in modo che l'applicazione non possa più fare riferimento o utilizzare il socket in alcun modo.

In Windows Sockets è possibile utilizzare sia la funzione [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) che la funzione [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) per avviare una sequenza di arresto, mentre la funzione [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) viene utilizzata per deallocare gli handle di socket e liberare le risorse associate. Tuttavia, si verifica una certa confusione dal fatto che la funzione **WSPCloseSocket** provocherà implicitamente la generazione di una sequenza di arresto, se non è già avvenuta. In realtà, si tratta di una pratica di programmazione piuttosto comune che si basa su questa funzionalità e si utilizza **WSPCloseSocket** per avviare la sequenza di arresto e deallocare l'handle del socket.

Per semplificare questo utilizzo, l'interfaccia di socket fornisce i controlli tramite il meccanismo dell'opzione socket che consente al programmatore di indicare se la sequenza di arresto implicita deve essere normale o interrotta e anche se la funzione deve rimanere incompleta, per consentire il completamento di una sequenza di arresto normale.

Se si stabiliscono i valori appropriati per le opzioni del socket in modo \_ che vengano sospesi e quindi \_ DONTLINGER, è possibile ottenere i tipi di comportamento seguenti con la funzione [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) .

-   Sequenza di arresto interrotta, ritorno immediato da [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Arresto normale, ritorno a ritardo fino al completamento della sequenza di arresto o intervallo di tempo specificato. Se l'intervallo di tempo scade prima del completamento della sequenza di arresto normale, viene eseguita una sequenza di arresto abortivo e [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) restituisce.
-   Normale arresto, restituire immediatamente e consentire il completamento della sequenza di arresto in background. Comportamento predefinito. Si noti, tuttavia, che l'applicazione non ha modo di sapere quando (o se) viene completata la sequenza di arresto normale.

Una tecnica che può essere usata per ridurre al minimo la possibilità di problemi che si verificano durante la connessione teardown non prevede l'avvio di un arresto implicito da parte di [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)). Viene invece utilizzata una delle due funzioni di arresto esplicite ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))). Questa operazione a sua volta causerà \_ la ricezione di un'indicazione di chiusura FD da parte dell'applicazione peer, a indicare che tutti i dati in sospeso sono stati ricevuti. Per illustrare questo problema, nella tabella seguente vengono illustrate le funzioni che verrebbero richiamate dai componenti client e server di un'applicazione, in cui il client è responsabile dell'avvio di un arresto normale.

| Lato client                                                                                                                         | Sul lato server                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) richiama [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD \_ Send) per segnalare la fine della sessione e il client non ha più dati da inviare. |                                                                                                              |
|                                                                                                                                     | (2) riceve \_ la chiusura FD, che indica l'arresto normale in corso e la ricezione di tutti i dati.        |
|                                                                                                                                     | (3) Invia tutti i dati di risposta rimanenti.                                                                       |
| (5') ottiene FD \_ Read e Invoke ricezione per ottenere tutti i dati di risposta inviati dal server.                                                         | (4) richiama [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD \_ Send) per indicare che il server non ha più dati da inviare. |
| (5) riceve l' \_ indicazione di chiusura FD.                                                                                                  | (4') richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

La sequenza temporale viene mantenuta dal passaggio (1) al passaggio (6) tra il client e il server. ad eccezione dei passaggi (4') e (5') che hanno solo un significato di intervallo locale nel senso che Step (5) segue Step (5') sul lato client mentre Step (4') segue Step (4) sul lato server, senza alcuna relazione temporale con la parte remota.

 

 
