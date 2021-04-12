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
# <a name="pgm-senders-and-receivers"></a><span data-ttu-id="cc505-103">Mittenti e ricevitori PGM</span><span class="sxs-lookup"><span data-stu-id="cc505-103">PGM Senders and Receivers</span></span>

<span data-ttu-id="cc505-104">La creazione di una sessione PGM è simile alla routine di creazione connessione associata a una sessione TCP.</span><span class="sxs-lookup"><span data-stu-id="cc505-104">Establishing a PGM session is similar to the connection establishment routine associated with a TCP session.</span></span> <span data-ttu-id="cc505-105">La partenza significativa da una sessione TCP, tuttavia, è che la semantica del client e del server è invertita. il server (il mittente PGM) si connette a un gruppo multicast, mentre il client (il ricevitore PGM) attende di accettare una connessione.</span><span class="sxs-lookup"><span data-stu-id="cc505-105">The significant departure from a TCP session, however, is that the client and server semantics are reversed; the server (the PGM sender) connects to a multicast group, while the client (the PGM receiver) waits to accept a connection.</span></span> <span data-ttu-id="cc505-106">I paragrafi seguenti illustrano i passaggi a livello di codice necessari per la creazione di un mittente PGM e un ricevitore PGM.</span><span class="sxs-lookup"><span data-stu-id="cc505-106">The following paragraphs detail programmatic steps necessary for creating a PGM sender and a PGM receiver.</span></span> <span data-ttu-id="cc505-107">Questa pagina descrive anche le modalità dati disponibili per le sessioni PGM.</span><span class="sxs-lookup"><span data-stu-id="cc505-107">This page also describes the available data modes for PGM sessions.</span></span>

## <a name="pgm-sender"></a><span data-ttu-id="cc505-108">Mittente PGM</span><span class="sxs-lookup"><span data-stu-id="cc505-108">PGM Sender</span></span>

<span data-ttu-id="cc505-109">**Per creare un mittente PGM, seguire questa procedura**</span><span class="sxs-lookup"><span data-stu-id="cc505-109">**To create a PGM sender, perform the following steps**</span></span>

1.  <span data-ttu-id="cc505-110">Creare un socket PGM.</span><span class="sxs-lookup"><span data-stu-id="cc505-110">Create a PGM socket.</span></span>
2.  <span data-ttu-id="cc505-111">[**associare**](/windows/desktop/api/winsock/nf-winsock-bind) il socket a tutti gli indirizzi \_ .</span><span class="sxs-lookup"><span data-stu-id="cc505-111">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to INADDR\_ANY.</span></span>
3.  <span data-ttu-id="cc505-112">[**connettersi**](/windows/desktop/api/Winsock2/nf-winsock2-connect) all'indirizzo di trasmissione del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="cc505-112">[**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) to the multicast group transmission address.</span></span>

<span data-ttu-id="cc505-113">Non viene eseguito alcun handshake della sessione formale con alcun client.</span><span class="sxs-lookup"><span data-stu-id="cc505-113">No formal session handshaking is performed with any clients.</span></span> <span data-ttu-id="cc505-114">Il processo di connessione è simile a quello di una [**connessione UDP,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)in quanto associa un indirizzo endpoint (gruppo multicast) al socket.</span><span class="sxs-lookup"><span data-stu-id="cc505-114">The connection process is similar to a UDP [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), in that it associates an endpoint address (the multicast group) with the socket.</span></span> <span data-ttu-id="cc505-115">Al termine, i dati possono essere inviati al socket.</span><span class="sxs-lookup"><span data-stu-id="cc505-115">Once completed, data may be sent on the socket.</span></span>

<span data-ttu-id="cc505-116">Quando un mittente crea un socket PGM e lo connette a un indirizzo multicast, viene creata una sessione PGM.</span><span class="sxs-lookup"><span data-stu-id="cc505-116">When a sender creates a PGM socket and connects it to a multicast address, a PGM session is created.</span></span> <span data-ttu-id="cc505-117">Una sessione multicast affidabile viene definita da una combinazione dell'identificatore univoco globale (GUID) e della porta di origine.</span><span class="sxs-lookup"><span data-stu-id="cc505-117">A reliable multicast session is defined by a combination of the globally unique identifier (GUID) and the source port.</span></span> <span data-ttu-id="cc505-118">Il GUID viene generato dal trasporto.</span><span class="sxs-lookup"><span data-stu-id="cc505-118">The GUID is generated by the transport.</span></span> <span data-ttu-id="cc505-119">La porta sSource viene specificata dal trasporto e non viene fornito alcun controllo su quale porta di origine viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cc505-119">The sSource port is specified by the transport, and no control is provided over which source port is used.</span></span>

> [!Note]  
> <span data-ttu-id="cc505-120">La ricezione di dati su un socket del mittente non è consentita e genera un errore.</span><span class="sxs-lookup"><span data-stu-id="cc505-120">Receiving data on a sender socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="cc505-121">Il frammento di codice seguente illustra la configurazione di un mittente PGM:</span><span class="sxs-lookup"><span data-stu-id="cc505-121">The following code snippet illustrates setting up a PGM sender:</span></span>


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



## <a name="pgm-receiver"></a><span data-ttu-id="cc505-122">Ricevitore PGM</span><span class="sxs-lookup"><span data-stu-id="cc505-122">PGM Receiver</span></span>

<span data-ttu-id="cc505-123">**Per creare un ricevitore PGM, seguire questa procedura**</span><span class="sxs-lookup"><span data-stu-id="cc505-123">**To create a PGM receiver, perform the following steps**</span></span>

1.  <span data-ttu-id="cc505-124">Creare un socket PGM.</span><span class="sxs-lookup"><span data-stu-id="cc505-124">Create a PGM socket.</span></span>
2.  <span data-ttu-id="cc505-125">[**associare**](/windows/desktop/api/winsock/nf-winsock-bind) il socket all'indirizzo del gruppo multicast su cui il mittente sta trasmettendo.</span><span class="sxs-lookup"><span data-stu-id="cc505-125">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to the multicast group address on which the sender is transmitting.</span></span>
3.  <span data-ttu-id="cc505-126">Chiamare la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) sul socket per attivare la modalità di ascolto del socket.</span><span class="sxs-lookup"><span data-stu-id="cc505-126">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function on the socket to put the socket in listening mode.</span></span> <span data-ttu-id="cc505-127">La funzione Listen restituisce quando viene rilevata una sessione PGM sull'indirizzo e sulla porta del gruppo multicast specificato.</span><span class="sxs-lookup"><span data-stu-id="cc505-127">The listen function returns when a PGM session is detected on the specified multicast group address and port.</span></span>
4.  <span data-ttu-id="cc505-128">Chiamare la funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) per ottenere un nuovo handle del socket corrispondente alla sessione.</span><span class="sxs-lookup"><span data-stu-id="cc505-128">Call the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function to obtain a new socket handle corresponding to the session.</span></span>

<span data-ttu-id="cc505-129">Solo i dati PGM originali (ODATA) attivano l'accettazione di una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="cc505-129">Only original PGM data (ODATA) triggers the acceptance of a new session.</span></span> <span data-ttu-id="cc505-130">Per questo motivo, è possibile che il trasporto riceva un altro traffico PGM (ad esempio, i pacchetti SPM o RDATA), ma che non comporti la restituzione della funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="cc505-130">As such, other PGM traffic (such as SPM or RDATA packets) may be received by the transport, but do not result in the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function returning.</span></span>

<span data-ttu-id="cc505-131">Una volta accettata una sessione, viene utilizzato l'handle del socket restituito per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="cc505-131">Once a session is accepted, the returned socket handle is used for receiving data.</span></span>

> [!Note]  
> <span data-ttu-id="cc505-132">L'invio di dati su un socket di ricezione non è consentito e genera un errore.</span><span class="sxs-lookup"><span data-stu-id="cc505-132">Sending data on a receive socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="cc505-133">Il frammento di codice seguente illustra la configurazione di un ricevitore PGM:</span><span class="sxs-lookup"><span data-stu-id="cc505-133">The following code snippet illustrates setting up a PGM receiver:</span></span>


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



## <a name="data-modes"></a><span data-ttu-id="cc505-134">Modalità dati</span><span class="sxs-lookup"><span data-stu-id="cc505-134">Data Modes</span></span>

<span data-ttu-id="cc505-135">Le sessioni PGM hanno due opzioni per le modalità dati, ovvero la modalità messaggio e la modalità flusso.</span><span class="sxs-lookup"><span data-stu-id="cc505-135">PGM sessions have two options for data modes: message mode and stream mode.</span></span>

<span data-ttu-id="cc505-136">La modalità messaggio è appropriata per le applicazioni che devono inviare messaggi discreti ed è specificata da un tipo socket di SOCK \_ RDM.</span><span class="sxs-lookup"><span data-stu-id="cc505-136">Message mode is appropriate for applications that need to send discrete messages, and is specified by a socket type of SOCK\_RDM.</span></span> <span data-ttu-id="cc505-137">La modalità flusso è appropriata per le applicazioni che devono inviare i dati di streaming ai destinatari, ad esempio applicazioni video o vocali, ed è specificato da un tipo di socket del \_ flusso Sock.</span><span class="sxs-lookup"><span data-stu-id="cc505-137">Stream mode is appropriate for applications that need to send streaming data to receivers, such as video or voice applications, and is specified by a socket type of SOCK\_STREAM.</span></span> <span data-ttu-id="cc505-138">La scelta degli effetti sulla modalità di elaborazione dei dati in Winsock.</span><span class="sxs-lookup"><span data-stu-id="cc505-138">The choice of mode effects how Winsock processes data.</span></span>

<span data-ttu-id="cc505-139">Si consideri l'esempio seguente: un mittente PGM in modalità messaggio esegue tre chiamate alla funzione [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , ognuna con un buffer di 100 byte.</span><span class="sxs-lookup"><span data-stu-id="cc505-139">Consider the following example: A message mode PGM sender makes three calls to the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) function, each with a 100-byte buffer.</span></span> <span data-ttu-id="cc505-140">Questa operazione viene visualizzata in transito come tre pacchetti PGM discreti.</span><span class="sxs-lookup"><span data-stu-id="cc505-140">This operation appears on the wire as three discrete PGM packets.</span></span> <span data-ttu-id="cc505-141">Sul lato ricevitore ogni chiamata alla funzione [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) restituisce solo 100 byte, anche se viene fornito un buffer di ricezione più grande.</span><span class="sxs-lookup"><span data-stu-id="cc505-141">On the receiver side, each call to the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) function returns only 100 bytes, even if a larger receive buffer is provided.</span></span> <span data-ttu-id="cc505-142">Al contrario, con un mittente PGM in modalità flusso, le trasmissioni di 3 100 byte potrebbero essere unite in meno di tre pacchetti fisici in transito (o fuse in un BLOB di dati sul lato ricevitore).</span><span class="sxs-lookup"><span data-stu-id="cc505-142">In contrast, with a stream mode PGM sender those three 100 byte transmissions could be coalesced into less than three physical packets on the wire (or coalesced into one blob of data on the receiver side).</span></span> <span data-ttu-id="cc505-143">Di conseguenza, quando il ricevitore chiama una delle funzioni di ricezione di Windows Sockets, qualsiasi quantità di dati ricevuta dal trasporto PGM può essere restituita all'applicazione senza considerare la modalità di trasmissione o ricezione fisica dei dati.</span><span class="sxs-lookup"><span data-stu-id="cc505-143">As such, when the receiver calls one of the Windows Sockets receive functions, any amount of data that has been received by the PGM transport may be returned to the application without regard to how the data was physically transmitted or received.</span></span>

 

 



