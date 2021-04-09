---
description: Di seguito viene descritto l'evento imprevisto per l'arresto di una connessione socket stabilita.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Arresto della connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbde0cfe4c3a97435c2412d28970107f830308fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879225"
---
# <a name="connection-shutdown"></a>Arresto della connessione

Di seguito viene descritto l'evento imprevisto per l'arresto di una connessione socket stabilita.

## <a name="initiating-shutdown-sequence"></a>Avvio della sequenza di arresto

Una connessione socket può essere disattivata in uno dei diversi modi. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) *(con uguale* a SD \_ Send o SD \_ Both) e [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) possono essere usati per avviare un normale arresto della connessione. [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) può essere usato per avviare un arresto normale o abortivo, a seconda delle opzioni Linger richiamate dalla chiusura di un socket. Vedere di seguito per altre informazioni sulle chiusure aggraziate e interrotte e sulle opzioni Linger.

## <a name="indicating-remote-shutdown"></a>Indicazione dell'arresto remoto

I provider di servizi indicano la connessione teardown avviata dalla parte remota tramite l' \_ evento di chiusura della rete FD. L'arresto normale è indicato anche tramite [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) quando il numero di byte letti è 0 per i protocolli di flusso di byte oppure tramite un codice di errore restituito di WSAEDISCON nativo per i protocolli orientati ai messaggi. In ogni caso, un codice di errore restituito da **WSPRecv** di WSAECONNRESET indica un arresto ininterrotto.

## <a name="exchanging-user-data-at-shutdown-time"></a>Scambio di dati utente al momento dell'arresto

Al momento della connessione teardown, è anche possibile (per i protocolli che lo supportano) per scambiare dati utente tra gli endpoint. La fine che avvia teardown può chiamare [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) per indicare che non è necessario inviare altri dati e causare l'avvio della sequenza di teardown di connessione. Per alcuni protocolli, parte di questa sequenza di teardown è il recapito dei dati di disconnessione dall'iniziatore teardown. Dopo aver ricevuto l'avviso che l'estremità remota ha avviato la sequenza teardown (in genere tramite l' \_ indicazione di chiusura FD), è possibile chiamare la funzione [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) per ricevere i dati di disconnessione (se presenti).

Per illustrare il modo in cui possono essere usati i dati di disconnessione, considerare lo scenario seguente. La metà client di un'applicazione client/server è responsabile della terminazione di una connessione socket. Coincidere con la terminazione fornita (tramite dati di disconnessione) il numero totale di transazioni elaborate con il server. Il server a sua volta risponde con il totale complessivo cumulativo di transazioni elaborate con tutti i client. La sequenza di chiamate e indicazioni potrebbe verificarsi come illustrato nella tabella seguente.

| Lato client                                                                                                               | Sul lato server                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) richiama [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) per concludere la sessione e fornire il totale della transazione.            |                                                                                                                                         |
|                                                                                                                           | (2) Ottiene \_ la chiusura FD o [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con un valore restituito pari a zero o WSAEDISCON nativo che indica l'arresto normale in corso. |
|                                                                                                                           | (3) richiama [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) per ottenere il totale della transazione del client.                                         |
|                                                                                                                           | (4) calcola il totale complessivo cumulativo di tutte le transazioni.                                                                                |
|                                                                                                                           | (5) richiama [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) per trasmettere il totale complessivo.                                                   |
| (6) riceve l' \_ indicazione di chiusura FD.                                                                                        | (5') richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) richiama [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) per ricevere e archiviare il totale complessivo delle transazioni. |                                                                                                                                         |
|                                                                                                                           | (8) richiama [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

Step (5') deve seguire step (5), ma non ha una relazione di intervallo con i passaggi (6), (7) o (8).

 

 
