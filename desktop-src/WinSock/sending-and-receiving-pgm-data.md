---
description: L'invio e la ricezione di dati PGM è simile all'invio o alla ricezione di dati su qualsiasi socket. Esistono considerazioni specifiche per la PGM, descritte nei paragrafi seguenti.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Invio e ricezione di dati PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 130b38ea52e5d0679b988e55f8292b9752a4bf15d0514a8277a2e0b3b2327001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740572"
---
# <a name="sending-and-receiving-pgm-data"></a>Invio e ricezione di dati PGM

L'invio e la ricezione di dati PGM è simile all'invio o alla ricezione di dati su qualsiasi socket. Esistono considerazioni specifiche per la PGM, descritte nei paragrafi seguenti.

## <a name="sending-pgm-data"></a>Invio di dati PGM

Dopo aver creato una sessione del mittente PGM, i dati vengono inviati usando le varie funzioni di invio Windows Sockets: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Poiché Windows handle Sockets sono file system handle, anche altre funzioni, ad esempio [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) e CRT, possono trasmettere dati. Il frammento di codice seguente illustra un'operazione del mittente PGM:


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



Quando si usa la modalità messaggio (SOCK RDM), ogni chiamata a una funzione di invio restituisce un messaggio discreto, che talvolta non è \_ consigliabile. Un'applicazione potrebbe voler inviare un messaggio di 2 MB con più chiamate per inviare . [](/windows/desktop/api/Winsock2/nf-winsock2-send) In questi casi, il mittente può impostare l'opzione [socket RM \_ SET MESSAGE \_ \_ BOUNDARY](socket-options.md) per indicare le dimensioni del messaggio che segue.

Se la finestra di invio è piena, un nuovo invio dall'applicazione non viene accettato fino a quando la finestra non è stata avanzata. Il tentativo di invio su un socket non bloccante ha esito negativo con WSAEWOULDBLOCK. un socket di blocco si blocca finché la finestra non avanza fino al punto in cui i dati richiesti possono essere memorizzati nel buffer e inviati. Nell'I/O sovrapposto, l'operazione non viene completata fino a quando la finestra non avanza sufficientemente per contenere i nuovi dati.

## <a name="receiving-pgm-data"></a>Ricezione di dati PGM

Dopo aver creato una sessione ricevitore PGM, i dati vengono ricevuti usando le varie funzioni di ricezione Windows Sockets: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Poiché Windows handle Sockets sono anche handle di file, le [**funzioni ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e CRT possono essere usate anche per ricevere dati di sessione PGM. Il trasporto inoltra i dati al ricevitore non appena arrivano, purché i dati sono in sequenza. Il trasporto garantisce che i dati restituiti siano contigui e senza duplicati. Il frammento di codice seguente illustra un'operazione di ricezione PGM:


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



Quando si usa la modalità messaggio (SOCK RDM), il trasporto indica quando viene ricevuto un messaggio parziale, con l'errore WSAEMSGSIZE o impostando il flag MSG PARTIAL al ritorno dalle funzioni \_ \_ [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) e [**WSARecvFrom.**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) Quando l'ultimo frammento del messaggio completo viene restituito al client, l'errore o il flag non viene indicato.

Quando la sessione viene terminata correttamente, l'operazione di ricezione ha esito negativo con WSAEDISCON. Quando si verifica una perdita di dati nel trasporto, PGM esegue temporaneamente il buffer dei pacchetti out-of-sequence e tenta di recuperare i dati persi. Se la perdita di dati non è irreversibile, l'operazione di ricezione ha esito negativo con WSAECONNRESET e la sessione viene terminata. La sessione può essere reimpostata a causa di diverse condizioni, tra cui le seguenti:

-   Il ricevitore o la velocità di connessione in ingresso è troppo lenta per tenere il passo con la velocità dei dati in ingresso.
-   Si verifica una perdita eccessiva di dati, probabilmente a causa di condizioni di rete temporanee, ad esempio problemi di routing, instabilità della rete e così via.
-   Si verifica un errore irreversibile nel mittente.
-   L'utilizzo eccessivo delle risorse si verifica nel computer locale, ad esempio superando l'archiviazione buffer interna massima consentita o riscontrando una condizione di risorse non disponibili.
-   Si verifica un errore di controllo di coerenza dei dati.
-   L'errore in un componente PGM dipende da, ad esempio TCP/IP o Windows Socket.

Sia il primo che il secondo elemento nell'elenco precedente potrebbero comportare l'esecuzione eccessiva del buffer da parte del ricevitore prima dell'eccesso di risorse o prima di andare oltre la finestra del mittente.

## <a name="terminating-a-pgm-session"></a>Chiusura di una sessione PGM

Il mittente o il destinatario PGM può interrompere l'invio o la ricezione di dati chiamando [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). Il ricevitore deve chiamare **closesocket** sui socket di ascolto e di ricezione per evitare perdite di gestione. La chiamata [**di shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) sul mittente prima di chiamare **closesocket** garantisce l'invio di tutti i dati e la manutenzione dei dati di ripristino fino a quando la finestra di invio non passa oltre l'ultima sequenza di dati, anche se l'applicazione stessa termina.

 

 
