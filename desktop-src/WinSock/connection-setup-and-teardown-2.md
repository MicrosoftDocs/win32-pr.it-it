---
description: La funzione WSAAccept consente a un'applicazione di ottenere informazioni sul chiamante, ad esempio l'identificatore del chiamante e la qualità del servizio, prima di decidere se accettare una richiesta di connessione in ingresso.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Configurazione della connessione e teardown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c4ac1f32524d097e11825f8104eb41fee3c528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307007"
---
# <a name="connection-setup-and-teardown"></a>Configurazione della connessione e teardown

La funzione [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) consente a un'applicazione di ottenere informazioni sul chiamante, ad esempio l'identificatore del chiamante e la qualità del servizio, prima di decidere se accettare una richiesta di connessione in ingresso. Questa operazione viene eseguita con un callback a una funzione di condizione fornita dall'applicazione.

I dati da utente a utente specificati dai parametri nella funzione [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) e la funzione Condition di [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) possono essere trasferiti al peer durante lo stabilimento della connessione, purché questa funzionalità sia supportata dal provider di servizi.

È anche possibile (per i protocolli che lo supportano) per scambiare dati utente tra gli endpoint al momento della connessione teardown. La fine che avvia teardown può chiamare la funzione [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) per indicare che non vengono inviati altri dati e per avviare la sequenza di teardown della connessione. Per alcuni protocolli, parte di teardown è la consegna dei dati di disconnessione dall'iniziatore teardown. Dopo aver ricevuto l'avviso che l'estremità remota ha avviato teardown (in genere dall' \_ indicazione di chiusura FD), è possibile chiamare la funzione [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) per ricevere i dati di disconnessione, se presenti.

Per illustrare il modo in cui è possibile usare i dati di disconnessione, considerare lo scenario seguente. La metà client di un'applicazione client/server è responsabile della terminazione di una connessione socket. In coincidenza con la terminazione, fornisce (usando i dati di disconnessione) il numero totale di transazioni elaborate con il server. Il server a sua volta risponde con il totale cumulativo delle transazioni elaborate con tutti i client. La sequenza di chiamate e indicazioni potrebbe verificarsi come segue:

| Lato client                                                                                                              | Sul lato server                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) richiamare [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) per terminare la sessione e fornire il totale della transazione.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) ottenere FD \_ Close, [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) con un valore restituito pari a zero oppure [WSAEDISCON nativo](windows-sockets-error-codes-2.md) error return from [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) che indica un normale arresto in corso. |
|                                                                                                                          | (3) richiamare [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) per ottenere il totale della transazione del client.                                                                                                                                |
|                                                                                                                          | (4) calcolo del totale complessivo cumulativo di tutte le transazioni.                                                                                                                                                                       |
|                                                                                                                          | (5) richiamare [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) per trasmettere il totale complessivo.                                                                                                                                          |
| (6) ricevere l' \_ indicazione di chiusura FD.                                                                                        | (5a) richiamare [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                                                                                                                             |
| (7) richiamare [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) per ricevere e archiviare il totale complessivo di transazioni cumulative. |                                                                                                                                                                                                                               |
| (8) richiamare [ **chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Si noti che Step (5a) deve seguire step (5), ma non ha alcuna relazione temporale con STEP (6), (7) o (8).

 

 



