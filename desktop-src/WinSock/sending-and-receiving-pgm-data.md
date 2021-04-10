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
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="3bc4e-104">Invio e ricezione di dati PGM</span><span class="sxs-lookup"><span data-stu-id="3bc4e-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="3bc4e-105">L'invio e la ricezione di dati PGM è simile all'invio o alla ricezione di dati in qualsiasi socket.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="3bc4e-106">Sono presenti considerazioni specifiche di PGM, descritte nei paragrafi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="3bc4e-107">Invio di dati PGM</span><span class="sxs-lookup"><span data-stu-id="3bc4e-107">Sending PGM Data</span></span>

<span data-ttu-id="3bc4e-108">Una volta creata la sessione del mittente PGM, i dati vengono inviati usando le varie funzioni di invio di Windows Sockets: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span><span class="sxs-lookup"><span data-stu-id="3bc4e-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="3bc4e-109">Poiché gli handle di Windows Sockets sono file system handle, altre funzioni quali funzioni [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) e CRT possono anche trasmettere dati.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="3bc4e-110">Il frammento di codice seguente illustra un'operazione del mittente PGM:</span><span class="sxs-lookup"><span data-stu-id="3bc4e-110">The following code snippet illustrates a PGM sender operation:</span></span>


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



<span data-ttu-id="3bc4e-111">Quando si usa la modalità messaggio (SOCK \_ RDM), ogni chiamata a una funzione Send genera un messaggio discreto, che talvolta non è auspicabile. un'applicazione potrebbe voler inviare un messaggio di 2 megabyte con più chiamate da [**inviare**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span><span class="sxs-lookup"><span data-stu-id="3bc4e-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="3bc4e-112">In tali circostanze, il mittente può impostare l'opzione del socket del [ \_ limite del \_ messaggio \_ di RM set](socket-options.md) per indicare le dimensioni del messaggio che segue.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="3bc4e-113">Se la finestra di trasmissione è piena, un nuovo invio dall'applicazione non viene accettato fino a quando non è stata avanzata la finestra.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="3bc4e-114">Il tentativo di invio su un socket non bloccante ha esito negativo con WSAEWOULDBLOCK; un socket di blocco viene semplicemente bloccato fino a quando la finestra non viene spostata nel punto in cui i dati richiesti possono essere memorizzati nel buffer e inviati.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="3bc4e-115">Nell'I/O sovrapposto, l'operazione non viene completata fino a quando la finestra non viene spostata in modo da contenere i nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="3bc4e-116">Ricezione di dati PGM</span><span class="sxs-lookup"><span data-stu-id="3bc4e-116">Receiving PGM Data</span></span>

<span data-ttu-id="3bc4e-117">Una volta creata la sessione del ricevitore PGM, i dati vengono ricevuti utilizzando le varie funzioni di ricezione di Windows Sockets: [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span><span class="sxs-lookup"><span data-stu-id="3bc4e-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="3bc4e-118">Poiché i socket di Windows sono anche handle di file, le funzioni [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e CRT possono essere utilizzate anche per ricevere dati della sessione PGM.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="3bc4e-119">Il trasporto invia i dati fino al ricevitore così come arrivano fino a quando i dati sono in sequenza.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="3bc4e-120">Il trasporto garantisce che i dati restituiti siano contigui e privi di duplicati.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="3bc4e-121">Nel frammento di codice seguente viene illustrata un'operazione di ricezione PGM:</span><span class="sxs-lookup"><span data-stu-id="3bc4e-121">The following code snippet illustrates a PGM receive operation:</span></span>


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



<span data-ttu-id="3bc4e-122">Quando si usa la modalità messaggio (SOCK \_ RDM), il trasporto indica quando viene ricevuto un messaggio parziale, con l'errore WSAEMSGSIZE o impostando il \_ flag parziale msg al ritorno dalle funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="3bc4e-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="3bc4e-123">Quando al client viene restituito l'ultimo frammento del messaggio completo, l'errore o il flag non è indicato.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="3bc4e-124">Quando la sessione viene terminata normalmente, l'operazione di ricezione ha esito negativo con WSAEDISCON nativo.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="3bc4e-125">Quando si verifica una perdita di dati nel trasporto, PGM memorizza temporaneamente i pacchetti fuori sequenza e tenta di recuperare i dati persi.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="3bc4e-126">Se la perdita di dati è irreversibile, l'operazione di ricezione ha esito negativo con WSAECONNRESET e la sessione viene terminata.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="3bc4e-127">La sessione può essere reimpostata a causa di una serie di condizioni, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="3bc4e-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="3bc4e-128">Il ricevitore o la velocità di connessione in ingresso è troppo lenta per restare al passo con la velocità dei dati in ingresso.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="3bc4e-129">Si verifica una perdita di dati eccessiva, probabilmente a causa di condizioni di rete transitorie, ad esempio problemi di routing, instabilità della rete e così via.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="3bc4e-130">Si è verificato un errore irreversibile sul mittente.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="3bc4e-131">Un utilizzo eccessivo delle risorse si verifica nel computer locale, ad esempio superando il valore massimo consentito per l'archiviazione del buffer interno oppure riscontrando una condizione di esaurimento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="3bc4e-132">Si verifica un errore di verifica della coerenza dei dati.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="3bc4e-133">Un errore in un componente PGM dipende da, ad esempio TCP/IP o Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="3bc4e-134">Sia il primo che il secondo elemento nell'elenco precedente possono comportare un sovraccarico del ricevitore prima di esaurire le risorse o prima di andare oltre la finestra del mittente.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="3bc4e-135">Terminazione di una sessione PGM</span><span class="sxs-lookup"><span data-stu-id="3bc4e-135">Terminating A PGM Session</span></span>

<span data-ttu-id="3bc4e-136">Il mittente o il destinatario PGM può arrestare l'invio o la ricezione dei dati chiamando [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span><span class="sxs-lookup"><span data-stu-id="3bc4e-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="3bc4e-137">Il ricevitore deve chiamare **chiamata closesocket** sia sui socket in ascolto che sulla ricezione per evitare perdite di handle.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="3bc4e-138">La chiamata di [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) sul mittente prima della chiamata a **chiamata closesocket** garantisce che tutti i dati vengano inviati e che i dati di ripristino vengano mantenuti fino a quando la finestra di trasmissione avanza oltre l'ultima sequenza di dati, anche se l'applicazione stessa termina.</span><span class="sxs-lookup"><span data-stu-id="3bc4e-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
