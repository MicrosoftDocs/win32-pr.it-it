---
description: La funzione WSAAccept consente a un'applicazione di ottenere informazioni sul chiamante, ad esempio l'identificatore del chiamante e la qualità del servizio prima di decidere se accettare una richiesta di connessione in ingresso.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Configurazione e rimozione della connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5e8c8a95c9baa90e95bd7b7da2702f3522b2a575d3d0181271428837e27b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051719"
---
# <a name="connection-setup-and-teardown"></a>Configurazione e rimozione della connessione

La [**funzione WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) consente a un'applicazione di ottenere informazioni sul chiamante, ad esempio l'identificatore del chiamante e la qualità del servizio prima di decidere se accettare una richiesta di connessione in ingresso. Questa operazione viene eseguita con un callback a una funzione di condizione fornita dall'applicazione.

I dati da utente a utente specificati dai parametri nella funzione [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) e nella funzione condition di [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) possono essere trasferiti al peer durante la creazione della connessione, a condizione che questa funzionalità sia supportata dal provider di servizi.

È anche possibile (per i protocolli che lo supportano) scambiare dati utente tra gli endpoint in fase di rimozione della connessione. L'estremità che avvia il teardown può chiamare la [**funzione WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) per indicare che non devono essere inviati altri dati e per avviare la sequenza di teardown della connessione. Per determinati protocolli, parte della rimozione è il recapito dei dati di disconnessione dall'iniziatore di teardown. Dopo aver ricevuto l'avviso che l'estremità remota ha avviato la rimozione (in genere tramite l'indicazione FD CLOSE), è possibile chiamare la funzione \_ [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) per ricevere i dati di disconnessione, se presenti.

Per illustrare come è possibile usare i dati di disconnessione, considerare lo scenario seguente. La metà client di un'applicazione client/server è responsabile della terminazione di una connessione socket. Coincidente con la terminazione, fornisce (usando i dati di disconnessione) il numero totale di transazioni elaborate con il server. Il server risponde a sua volta con il totale cumulativo delle transazioni elaborate con tutti i client. La sequenza di chiamate e indicazioni può verificarsi come segue:

| Lato client                                                                                                              | Sul lato server                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) Richiamare [**WSASendDisconnect per**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) chiudere la sessione e fornire il totale delle transazioni.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) Ottenere FD CLOSE, recv con valore restituito pari a zero o errore \_ [WSAEDISCON](windows-sockets-error-codes-2.md) restituito da [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) che indica l'arresto normale in corso. [](/windows/desktop/api/winsock/nf-winsock-recv) |
|                                                                                                                          | (3) Richiamare [**WSARecvDisconnect per**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) ottenere il totale delle transazioni del client.                                                                                                                                |
|                                                                                                                          | (4) Calcolare il totale complessivo cumulativo di tutte le transazioni.                                                                                                                                                                       |
|                                                                                                                          | (5) Richiamare [**WSASendDisconnect per**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) trasmettere il totale complessivo.                                                                                                                                          |
| (6) Ricevere l'indicazione FD \_ CLOSE.                                                                                        | (5a) Richiamare [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                                                                                                                             |
| (7) Richiamare [**WSARecvDisconnect per**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) ricevere e archiviare il totale complessivo cumulativo delle transazioni. |                                                                                                                                                                                                                               |
| (8) Richiamare [ **closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Si noti che il passaggio (5a) deve seguire il passaggio (5), ma non ha alcuna relazione di temporizzazione con il passaggio (6), (7) o (8).

 

 



