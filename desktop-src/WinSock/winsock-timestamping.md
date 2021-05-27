---
title: Timestamp di Winsock
description: I timestamp dei pacchetti sono una funzionalità fondamentale per molte applicazioni di sincronizzazione dell'orologio, &mdash; ad esempio Precision Time Protocol. Più vicina è la generazione di timestamp quando un pacchetto viene ricevuto/inviato dall'hardware della scheda di rete, più accurata è l'applicazione di sincronizzazione.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559958"
---
# <a name="winsock-timestamping"></a><span data-ttu-id="69a8e-104">Timestamp di Winsock</span><span class="sxs-lookup"><span data-stu-id="69a8e-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="69a8e-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="69a8e-105">Introduction</span></span>

<span data-ttu-id="69a8e-106">I timestamp dei pacchetti sono una funzionalità fondamentale per molte applicazioni di sincronizzazione dell'orologio, &mdash; ad esempio Precision Time Protocol.</span><span class="sxs-lookup"><span data-stu-id="69a8e-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="69a8e-107">Più vicina è la generazione di timestamp quando un pacchetto viene ricevuto/inviato dall'hardware della scheda di rete, più accurata è l'applicazione di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="69a8e-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="69a8e-108">Le API di timestamping descritte in questo argomento forniscono quindi all'applicazione un meccanismo per segnalare i timestamp generati ben al di sotto del livello dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69a8e-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="69a8e-109">In particolare, un timestamp software nell'interfaccia tra miniport e NDIS e un timestamp hardware nell'hardware della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="69a8e-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="69a8e-110">L'API timestamp può migliorare notevolmente l'accuratezza della sincronizzazione dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="69a8e-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="69a8e-111">Attualmente, l'ambito del supporto è quello dei socket UDP (User Datagram Protocol).</span><span class="sxs-lookup"><span data-stu-id="69a8e-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="69a8e-112">Timestamp di ricezione</span><span class="sxs-lookup"><span data-stu-id="69a8e-112">Receive timestamps</span></span>

<span data-ttu-id="69a8e-113">È possibile configurare la ricezione del timestamp di ricezione [**tramite SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="69a8e-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="69a8e-114">Usare tale IOCTL per abilitare la ricezione del timestamp di ricezione.</span><span class="sxs-lookup"><span data-stu-id="69a8e-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="69a8e-115">Quando si riceve un datagramma usando la [**funzione LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) il relativo timestamp (se disponibile) è contenuto nel messaggio SO_TIMESTAMP **controllo.**</span><span class="sxs-lookup"><span data-stu-id="69a8e-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="69a8e-116">**SO_TIMESTAMP** (0x300A) è definito in `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="69a8e-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="69a8e-117">I dati del messaggio di controllo vengono restituiti come **UINT64.**</span><span class="sxs-lookup"><span data-stu-id="69a8e-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="69a8e-118">Trasmettere i timestamp</span><span class="sxs-lookup"><span data-stu-id="69a8e-118">Transmit timestamps</span></span>

<span data-ttu-id="69a8e-119">La ricezione del timestamp di trasmissione viene configurata [**anche SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="69a8e-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="69a8e-120">Usare tale IOCTL per abilitare la ricezione del timestamp di trasmissione e specificare il numero di timestamp di trasmissione che verranno memorizzati nel buffer dal sistema.</span><span class="sxs-lookup"><span data-stu-id="69a8e-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="69a8e-121">Quando vengono generati, i timestamp di trasmissione vengono aggiunti al buffer.</span><span class="sxs-lookup"><span data-stu-id="69a8e-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="69a8e-122">Se il buffer è pieno, i nuovi timestamp di trasmissione vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="69a8e-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="69a8e-123">Quando si invia un datagramma, associare il datagramma a un messaggio **SO_TIMESTAMP_ID** di controllo.</span><span class="sxs-lookup"><span data-stu-id="69a8e-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="69a8e-124">Deve contenere un identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="69a8e-124">This should contain a unique identifier.</span></span> <span data-ttu-id="69a8e-125">Inviare il datagramma, insieme al relativo **SO_TIMESTAMP_ID** di controllo, usando [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span><span class="sxs-lookup"><span data-stu-id="69a8e-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="69a8e-126">I timestamp di trasmissione potrebbero non essere immediatamente disponibili dopo il ritorno di **WSASendMsg.**</span><span class="sxs-lookup"><span data-stu-id="69a8e-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="69a8e-127">Quando i timestamp di trasmissione diventano disponibili, vengono inseriti in un buffer per socket.</span><span class="sxs-lookup"><span data-stu-id="69a8e-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="69a8e-128">Usare il [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL per eseguire il polling del timestamp in base al relativo ID.</span><span class="sxs-lookup"><span data-stu-id="69a8e-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="69a8e-129">Se il timestamp è disponibile, viene rimosso dal buffer e restituito.</span><span class="sxs-lookup"><span data-stu-id="69a8e-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="69a8e-130">Se il timestamp non è disponibile, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) restituisce **WSAEWOULDBLOCK**.</span><span class="sxs-lookup"><span data-stu-id="69a8e-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="69a8e-131">Se viene generato un timestamp di trasmissione mentre il buffer è pieno, il nuovo timestamp viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="69a8e-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="69a8e-132">**SO_TIMESTAMP_ID** (0x300B) è definito in `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="69a8e-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="69a8e-133">È necessario fornire i dati del messaggio di controllo come **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="69a8e-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="69a8e-134">I timestamp sono rappresentati come valore del contatore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="69a8e-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="69a8e-135">La frequenza del contatore dipende dall'origine del timestamp.</span><span class="sxs-lookup"><span data-stu-id="69a8e-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="69a8e-136">Per i timestamp software, il contatore è un [**valore QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) ed è possibile determinarne la frequenza [**tramite QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span><span class="sxs-lookup"><span data-stu-id="69a8e-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="69a8e-137">Per i timestamp hardware nic, la frequenza del contatore dipende dall'hardware della scheda di interfaccia di rete ed è possibile determinarla con informazioni aggiuntive fornite da [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span><span class="sxs-lookup"><span data-stu-id="69a8e-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="69a8e-138">Per determinare l'origine dei timestamp, usare le [**funzioni GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) e [**GetInterfaceSupportedTimestampCapabilities.**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)</span><span class="sxs-lookup"><span data-stu-id="69a8e-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="69a8e-139">Oltre alla configurazione a livello di socket usando l'opzione [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket per abilitare la ricezione di timestamp per un socket, è necessaria anche la configurazione a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="69a8e-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="69a8e-140">Stima della latenza del percorso di invio socket</span><span class="sxs-lookup"><span data-stu-id="69a8e-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="69a8e-141">In questa sezione verranno utilizzati timestamp di trasmissione per stimare la latenza del percorso di invio del socket.</span><span class="sxs-lookup"><span data-stu-id="69a8e-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="69a8e-142">Se si dispone di un'applicazione esistente che utilizza timestamp di I/O a livello di applicazione in cui il timestamp deve essere il più vicino possibile al punto di trasmissione effettivo, questo esempio fornisce una descrizione quantitativa di quanto le API di timestamp Di Winsock possano migliorare l'accuratezza &mdash; &mdash; dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69a8e-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="69a8e-143">L'esempio presuppone che nel sistema sia presente una sola scheda di interfaccia di rete (NIC) e che *interfaceLuid* sia il LUID di tale scheda.</span><span class="sxs-lookup"><span data-stu-id="69a8e-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="69a8e-144">Stima della latenza del percorso di ricezione socket</span><span class="sxs-lookup"><span data-stu-id="69a8e-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="69a8e-145">Ecco un esempio simile per il percorso di ricezione.</span><span class="sxs-lookup"><span data-stu-id="69a8e-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="69a8e-146">L'esempio presuppone che nel sistema sia presente una sola scheda di interfaccia di rete (NIC) e che *interfaceLuid* sia il LUID di tale scheda.</span><span class="sxs-lookup"><span data-stu-id="69a8e-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a><span data-ttu-id="69a8e-147">Una limitazione</span><span class="sxs-lookup"><span data-stu-id="69a8e-147">A limitation</span></span>

<span data-ttu-id="69a8e-148">Una limitazione delle API di timestamp di Winsock è che la chiamata SIO_GET_TX_TIMESTAMP [**è**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) sempre un'operazione non bloccante.</span><span class="sxs-lookup"><span data-stu-id="69a8e-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="69a8e-149">Anche la chiamata di IOCTL in modalità OVERLAPPED comporta un ritorno immediato di **WSAEWOULDBLOCK** se non sono attualmente disponibili timestamp di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="69a8e-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="69a8e-150">Poiché i timestamp di trasmissione potrebbero non essere immediatamente disponibili dopo il ritorno di [**WSASendMsg,**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) l'applicazione deve eseguire il polling di IOCTL fino a quando il timestamp non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="69a8e-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="69a8e-151">È garantito che un timestamp di trasmissione sia disponibile dopo una chiamata **WSASendMsg** riuscita, dato che il buffer del timestamp di trasmissione non è pieno.</span><span class="sxs-lookup"><span data-stu-id="69a8e-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>
