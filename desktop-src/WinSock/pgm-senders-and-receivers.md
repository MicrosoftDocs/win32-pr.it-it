---
description: La definizione di una sessione PGM è simile alla routine di creazione della connessione associata a una sessione TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Mittenti e ricevitori PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559ac30ace4374b48c86efeb579e1426cc455b00adb803e97244a37d8df7fda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741068"
---
# <a name="pgm-senders-and-receivers"></a>Mittenti e ricevitori PGM

La definizione di una sessione PGM è simile alla routine di creazione della connessione associata a una sessione TCP. La differenza significativa da una sessione TCP, tuttavia, è che la semantica del client e del server viene inversa; il server (mittente PGM) si connette a un gruppo multicast, mentre il client (ricevitore PGM) attende di accettare una connessione. I paragrafi seguenti illustrano in dettaglio i passaggi a livello di codice necessari per la creazione di un mittente PGM e di un ricevitore PGM. Questa pagina descrive anche le modalità dati disponibili per le sessioni PGM.

## <a name="pgm-sender"></a>Mittente PGM

**Per creare un mittente PGM, seguire questa procedura**

1.  Creare un socket PGM.
2.  [**associare**](/windows/desktop/api/winsock/nf-winsock-bind) il socket a INADDR \_ ANY.
3.  [**connettersi**](/windows/desktop/api/Winsock2/nf-winsock2-connect) all'indirizzo di trasmissione del gruppo multicast.

Nessun handshaking di sessione formale viene eseguito con i client. Il processo di connessione è simile a [**una**](/windows/desktop/api/Winsock2/nf-winsock2-connect)connessione UDP, in quanto associa un indirizzo endpoint (il gruppo multicast) al socket. Al termine, i dati possono essere inviati sul socket.

Quando un mittente crea un socket PGM e lo connette a un indirizzo multicast, viene creata una sessione PGM. Una sessione multicast affidabile è definita da una combinazione dell'identificatore univoco globale (GUID) e della porta di origine. Il GUID viene generato dal trasporto. La porta sSource viene specificata dal trasporto e non viene fornito alcun controllo sulla porta di origine usata.

> [!Note]  
> La ricezione di dati in un socket del mittente non è consentita e viene generato un errore.

 

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
2.  [**associare**](/windows/desktop/api/winsock/nf-winsock-bind) il socket all'indirizzo del gruppo multicast su cui il mittente trasmette.
3.  Chiamare la [**funzione di**](/windows/desktop/api/Winsock2/nf-winsock2-listen) ascolto sul socket per impostare il socket in modalità di ascolto. La funzione listen restituisce quando viene rilevata una sessione PGM sull'indirizzo e sulla porta del gruppo multicast specificati.
4.  Chiamare la [**funzione accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) per ottenere un nuovo handle socket corrispondente alla sessione.

Solo i dati PGM originali (ODATA) attivano l'accettazione di una nuova sessione. Di conseguenza, altro traffico PGM (ad esempio pacchetti SPM o RDATA) può essere ricevuto dal trasporto, ma non comporta la restituzione della funzione [**di**](/windows/desktop/api/Winsock2/nf-winsock2-listen) ascolto.

Dopo l'accettazione di una sessione, l'handle socket restituito viene usato per la ricezione dei dati.

> [!Note]  
> L'invio di dati in un socket di ricezione non è consentito e comporta un errore.

 

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

Le sessioni PGM hanno due opzioni per le modalità dati: modalità messaggio e modalità flusso.

La modalità messaggio è appropriata per le applicazioni che devono inviare messaggi discreti e viene specificata da un tipo di socket \_ RDM SOCK. La modalità flusso è appropriata per le applicazioni che devono inviare dati di streaming ai ricevitori, ad esempio applicazioni video o vocali, ed è specificata da un tipo di socket SOCK \_ STREAM. La scelta della modalità ha effetto sul modo in cui Winsock elabora i dati.

Si consideri l'esempio seguente: un mittente PGM in modalità messaggio effettua tre chiamate alla [**funzione WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ognuna con un buffer di 100 byte. Questa operazione viene visualizzata in transito come tre pacchetti PGM discreti. Sul lato ricevitore, ogni chiamata alla [**funzione WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) restituisce solo 100 byte, anche se viene fornito un buffer di ricezione più grande. Al contrario, con un mittente PGM in modalità flusso, queste tre trasmissioni da 100 byte possono essere coalizzate in meno di tre pacchetti fisici in transito (o coalesced in un unico BLOB di dati sul lato ricevitore). Di conseguenza, quando il ricevitore chiama una delle funzioni di ricezione Windows Sockets, qualsiasi quantità di dati ricevuti dal trasporto PGM può essere restituita all'applicazione indipendentemente dal modo in cui i dati sono stati trasmessi o ricevuti fisicamente.

 

 



