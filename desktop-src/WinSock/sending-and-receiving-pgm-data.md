---
description: L'invio e la ricezione di dati PGM è simile all'invio o alla ricezione di dati in qualsiasi socket. Sono presenti considerazioni specifiche di PGM, descritte nei paragrafi seguenti.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Invio e ricezione di dati PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131167"
---
# <a name="sending-and-receiving-pgm-data"></a>Invio e ricezione di dati PGM

L'invio e la ricezione di dati PGM è simile all'invio o alla ricezione di dati in qualsiasi socket. Sono presenti considerazioni specifiche di PGM, descritte nei paragrafi seguenti.

## <a name="sending-pgm-data"></a>Invio di dati PGM

Una volta creata la sessione del mittente PGM, i dati vengono inviati usando le varie funzioni di invio di Windows Sockets: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Poiché gli handle di Windows Sockets sono file system handle, altre funzioni quali funzioni [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) e CRT possono anche trasmettere dati. Il frammento di codice seguente illustra un'operazione del mittente PGM:


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



Quando si usa la modalità messaggio (SOCK \_ RDM), ogni chiamata a una funzione Send genera un messaggio discreto, che talvolta non è auspicabile. un'applicazione potrebbe voler inviare un messaggio di 2 megabyte con più chiamate da [**inviare**](/windows/desktop/api/Winsock2/nf-winsock2-send). In tali circostanze, il mittente può impostare l'opzione del socket del [ \_ limite del \_ messaggio \_ di RM set](socket-options.md) per indicare le dimensioni del messaggio che segue.

Se la finestra di trasmissione è piena, un nuovo invio dall'applicazione non viene accettato fino a quando non è stata avanzata la finestra. Il tentativo di invio su un socket non bloccante ha esito negativo con WSAEWOULDBLOCK; un socket di blocco viene semplicemente bloccato fino a quando la finestra non viene spostata nel punto in cui i dati richiesti possono essere memorizzati nel buffer e inviati. Nell'I/O sovrapposto, l'operazione non viene completata fino a quando la finestra non viene spostata in modo da contenere i nuovi dati.

## <a name="receiving-pgm-data"></a>Ricezione di dati PGM

Una volta creata la sessione del ricevitore PGM, i dati vengono ricevuti utilizzando le varie funzioni di ricezione di Windows Sockets: [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Poiché i socket di Windows sono anche handle di file, le funzioni [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e CRT possono essere utilizzate anche per ricevere dati della sessione PGM. Il trasporto invia i dati fino al ricevitore così come arrivano fino a quando i dati sono in sequenza. Il trasporto garantisce che i dati restituiti siano contigui e privi di duplicati. Nel frammento di codice seguente viene illustrata un'operazione di ricezione PGM:


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



Quando si usa la modalità messaggio (SOCK \_ RDM), il trasporto indica quando viene ricevuto un messaggio parziale, con l'errore WSAEMSGSIZE o impostando il \_ flag parziale msg al ritorno dalle funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) . Quando al client viene restituito l'ultimo frammento del messaggio completo, l'errore o il flag non è indicato.

Quando la sessione viene terminata normalmente, l'operazione di ricezione ha esito negativo con WSAEDISCON nativo. Quando si verifica una perdita di dati nel trasporto, PGM memorizza temporaneamente i pacchetti fuori sequenza e tenta di recuperare i dati persi. Se la perdita di dati è irreversibile, l'operazione di ricezione ha esito negativo con WSAECONNRESET e la sessione viene terminata. La sessione può essere reimpostata a causa di una serie di condizioni, incluse le seguenti:

-   Il ricevitore o la velocità di connessione in ingresso è troppo lenta per restare al passo con la velocità dei dati in ingresso.
-   Si verifica una perdita di dati eccessiva, probabilmente a causa di condizioni di rete transitorie, ad esempio problemi di routing, instabilità della rete e così via.
-   Si è verificato un errore irreversibile sul mittente.
-   Un utilizzo eccessivo delle risorse si verifica nel computer locale, ad esempio superando il valore massimo consentito per l'archiviazione del buffer interno oppure riscontrando una condizione di esaurimento delle risorse.
-   Si verifica un errore di verifica della coerenza dei dati.
-   Un errore in un componente PGM dipende da, ad esempio TCP/IP o Windows Sockets.

Sia il primo che il secondo elemento nell'elenco precedente possono comportare un sovraccarico del ricevitore prima di esaurire le risorse o prima di andare oltre la finestra del mittente.

## <a name="terminating-a-pgm-session"></a>Terminazione di una sessione PGM

Il mittente o il destinatario PGM può arrestare l'invio o la ricezione dei dati chiamando [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). Il ricevitore deve chiamare **chiamata closesocket** sia sui socket in ascolto che sulla ricezione per evitare perdite di handle. La chiamata di [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) sul mittente prima della chiamata a **chiamata closesocket** garantisce che tutti i dati vengano inviati e che i dati di ripristino vengano mantenuti fino a quando la finestra di trasmissione avanza oltre l'ultima sequenza di dati, anche se l'applicazione stessa termina.

 

 
