---
description: Di seguito viene descritto l'evento imprevisto delle operazioni per arrestare una connessione socket stabilita.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Arresto della connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbd26716c255c83a8ecc17305d9e59676645739a6f90d18ac72b5bcda49241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898421"
---
# <a name="connection-shutdown"></a>Arresto della connessione

Di seguito viene descritto l'evento imprevisto delle operazioni per arrestare una connessione socket stabilita.

## <a name="initiating-shutdown-sequence"></a>Avvio della sequenza di arresto

Una connessione socket può essere erta in uno dei modi seguenti. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (con uguale a SD SEND o SD BOTH) e  \_ \_ [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) possono essere usati per avviare un arresto normale della connessione. [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) può essere usato per avviare un arresto normale o abortivo, a seconda delle opzioni di blocco richiamate dalla chiusura di un socket. Per altre informazioni sugli arresti corretti e abortivi e sulle opzioni di blocco, vedere di seguito.

## <a name="indicating-remote-shutdown"></a>Che indica l'arresto remoto

I provider di servizi indicano la rimozione della connessione avviata dall'entità remota tramite l'evento di rete FD \_ CLOSE. L'arresto normale viene indicato anche tramite [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) quando il numero di byte letti è 0 per i protocolli di flusso di byte o tramite un codice di errore restituito di WSAEDISCON per i protocolli orientati ai messaggi. In ogni caso, un codice di errore restituito da WSAECONNRESET WSAECONNRESET indica un arresto non corretto. 

## <a name="exchanging-user-data-at-shutdown-time"></a>Scambio di dati utente in fase di arresto

Al momento della rimozione della connessione, è anche possibile (per i protocolli che lo supportano) scambiare i dati utente tra gli endpoint. L'estremità che avvia l'operazione di rimozione può chiamare [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) per indicare che non devono essere inviati altri dati e che la sequenza di teardown della connessione viene avviata. Per determinati protocolli, parte di questa sequenza di teardown è il recapito dei dati di disconnessione dall'iniziatore di teardown. Dopo aver ricevuto l'avviso che l'estremità remota ha avviato la sequenza di rimozione (in genere tramite l'indicazione FD CLOSE), è possibile chiamare la funzione \_ [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) per ricevere i dati di disconnessione (se presenti).

Per illustrare l'uso dei dati di disconnessione, considerare lo scenario seguente. La metà client di un'applicazione client/server è responsabile della terminazione di una connessione socket. Coincidente con la terminazione che fornisce (tramite dati di disconnessione) il numero totale di transazioni elaborate con il server. Il server risponde a sua volta con il totale complessivo cumulativo delle transazioni elaborate con tutti i client. La sequenza di chiamate e indicazioni può verificarsi come illustrato nella tabella seguente.

| Lato client                                                                                                               | Sul lato server                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) Richiama [**WSPSendDisconnect per**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) chiudere la sessione e fornire il totale della transazione.            |                                                                                                                                         |
|                                                                                                                           | (2) Ottiene FD \_ CLOSE o [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con valore restituito pari a zero o WSAEDISCON che indica l'arresto normale in corso. |
|                                                                                                                           | (3) Richiama [**WSPRecvDisconnect per**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) ottenere il totale delle transazioni del client.                                         |
|                                                                                                                           | (4) Calcola il totale complessivo cumulativo di tutte le transazioni.                                                                                |
|                                                                                                                           | (5) Richiama [**WSPSendDisconnect per**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) trasmettere il totale complessivo.                                                   |
| (6) Riceve l'indicazione FD \_ CLOSE.                                                                                        | (5') Richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) Richiama [**WSPRecvDisconnect per**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) ricevere e archiviare il totale complessivo cumulativo delle transazioni. |                                                                                                                                         |
|                                                                                                                           | (8) Richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

Il passaggio (5') deve seguire il passaggio (5), ma non ha alcuna relazione di temporizzazione con i passaggi (6), (7) o (8).

 

 
