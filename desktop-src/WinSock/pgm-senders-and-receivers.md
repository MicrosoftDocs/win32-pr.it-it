---
description: La creazione di una sessione PGM è simile alla routine di creazione connessione associata a una sessione TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Mittenti e ricevitori PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526119"
---
# <a name="pgm-senders-and-receivers"></a>Mittenti e ricevitori PGM

La creazione di una sessione PGM è simile alla routine di creazione connessione associata a una sessione TCP. La partenza significativa da una sessione TCP, tuttavia, è che la semantica del client e del server è invertita. il server (il mittente PGM) si connette a un gruppo multicast, mentre il client (il ricevitore PGM) attende di accettare una connessione. I paragrafi seguenti illustrano i passaggi a livello di codice necessari per la creazione di un mittente PGM e un ricevitore PGM. Questa pagina descrive anche le modalità dati disponibili per le sessioni PGM.

## <a name="pgm-sender"></a>Mittente PGM

**Per creare un mittente PGM, seguire questa procedura**

1.  Creare un socket PGM.
2.  [**associare**](/windows/desktop/api/winsock/nf-winsock-bind) il socket a tutti gli indirizzi \_ .
3.  [**connettersi**](/windows/desktop/api/Winsock2/nf-winsock2-connect) all'indirizzo di trasmissione del gruppo multicast.

Non viene eseguito alcun handshake della sessione formale con alcun client. Il processo di connessione è simile a quello di una [**connessione UDP,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)in quanto associa un indirizzo endpoint (gruppo multicast) al socket. Al termine, i dati possono essere inviati al socket.

Quando un mittente crea un socket PGM e lo connette a un indirizzo multicast, viene creata una sessione PGM. Una sessione multicast affidabile viene definita da una combinazione dell'identificatore univoco globale (GUID) e della porta di origine. Il GUID viene generato dal trasporto. La porta sSource viene specificata dal trasporto e non viene fornito alcun controllo su quale porta di origine viene utilizzata.

> [!Note]  
> La ricezione di dati su un socket del mittente non è consentita e genera un errore.

 

Il frammento di codice seguente illustra la configurazione di un mittente PGM:


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>Ricevitore PGM

**Per creare un ricevitore PGM, seguire questa procedura**

1.  Creare un socket PGM.
2.  [**associare**](/windows/desktop/api/winsock/nf-winsock-bind) il socket all'indirizzo del gruppo multicast su cui il mittente sta trasmettendo.
3.  Chiamare la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) sul socket per attivare la modalità di ascolto del socket. La funzione Listen restituisce quando viene rilevata una sessione PGM sull'indirizzo e sulla porta del gruppo multicast specificato.
4.  Chiamare la funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) per ottenere un nuovo handle del socket corrispondente alla sessione.

Solo i dati PGM originali (ODATA) attivano l'accettazione di una nuova sessione. Per questo motivo, è possibile che il trasporto riceva un altro traffico PGM (ad esempio, i pacchetti SPM o RDATA), ma che non comporti la restituzione della funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .

Una volta accettata una sessione, viene utilizzato l'handle del socket restituito per la ricezione dei dati.

> [!Note]  
> L'invio di dati su un socket di ricezione non è consentito e genera un errore.

 

Il frammento di codice seguente illustra la configurazione di un ricevitore PGM:


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>Modalità dati

Le sessioni PGM hanno due opzioni per le modalità dati, ovvero la modalità messaggio e la modalità flusso.

La modalità messaggio è appropriata per le applicazioni che devono inviare messaggi discreti ed è specificata da un tipo socket di SOCK \_ RDM. La modalità flusso è appropriata per le applicazioni che devono inviare i dati di streaming ai destinatari, ad esempio applicazioni video o vocali, ed è specificato da un tipo di socket del \_ flusso Sock. La scelta degli effetti sulla modalità di elaborazione dei dati in Winsock.

Si consideri l'esempio seguente: un mittente PGM in modalità messaggio esegue tre chiamate alla funzione [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , ognuna con un buffer di 100 byte. Questa operazione viene visualizzata in transito come tre pacchetti PGM discreti. Sul lato ricevitore ogni chiamata alla funzione [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) restituisce solo 100 byte, anche se viene fornito un buffer di ricezione più grande. Al contrario, con un mittente PGM in modalità flusso, le trasmissioni di 3 100 byte potrebbero essere unite in meno di tre pacchetti fisici in transito (o fuse in un BLOB di dati sul lato ricevitore). Di conseguenza, quando il ricevitore chiama una delle funzioni di ricezione di Windows Sockets, qualsiasi quantità di dati ricevuta dal trasporto PGM può essere restituita all'applicazione senza considerare la modalità di trasmissione o ricezione fisica dei dati.

 

 



