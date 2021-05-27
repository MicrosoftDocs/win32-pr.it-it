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
# <a name="winsock-timestamping"></a>Timestamp di Winsock

## <a name="introduction"></a>Introduzione

I timestamp dei pacchetti sono una funzionalità fondamentale per molte applicazioni di sincronizzazione dell'orologio, &mdash; ad esempio Precision Time Protocol. Più vicina è la generazione di timestamp quando un pacchetto viene ricevuto/inviato dall'hardware della scheda di rete, più accurata è l'applicazione di sincronizzazione.

Le API di timestamping descritte in questo argomento forniscono quindi all'applicazione un meccanismo per segnalare i timestamp generati ben al di sotto del livello dell'applicazione. In particolare, un timestamp software nell'interfaccia tra miniport e NDIS e un timestamp hardware nell'hardware della scheda di interfaccia di rete. L'API timestamp può migliorare notevolmente l'accuratezza della sincronizzazione dell'orologio. Attualmente, l'ambito del supporto è quello dei socket UDP (User Datagram Protocol).

## <a name="receive-timestamps"></a>Timestamp di ricezione

È possibile configurare la ricezione del timestamp di ricezione [**tramite SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Usare tale IOCTL per abilitare la ricezione del timestamp di ricezione. Quando si riceve un datagramma usando la [**funzione LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) il relativo timestamp (se disponibile) è contenuto nel messaggio SO_TIMESTAMP **controllo.**

**SO_TIMESTAMP** (0x300A) è definito in `mstcpip.h` . I dati del messaggio di controllo vengono restituiti come **UINT64.**

## <a name="transmit-timestamps"></a>Trasmettere i timestamp

La ricezione del timestamp di trasmissione viene configurata [**anche SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Usare tale IOCTL per abilitare la ricezione del timestamp di trasmissione e specificare il numero di timestamp di trasmissione che verranno memorizzati nel buffer dal sistema. Quando vengono generati, i timestamp di trasmissione vengono aggiunti al buffer. Se il buffer è pieno, i nuovi timestamp di trasmissione vengono eliminati.

Quando si invia un datagramma, associare il datagramma a un messaggio **SO_TIMESTAMP_ID** di controllo. Deve contenere un identificatore univoco. Inviare il datagramma, insieme al relativo **SO_TIMESTAMP_ID** di controllo, usando [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg). I timestamp di trasmissione potrebbero non essere immediatamente disponibili dopo il ritorno di **WSASendMsg.** Quando i timestamp di trasmissione diventano disponibili, vengono inseriti in un buffer per socket. Usare il [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL per eseguire il polling del timestamp in base al relativo ID. Se il timestamp è disponibile, viene rimosso dal buffer e restituito. Se il timestamp non è disponibile, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) restituisce **WSAEWOULDBLOCK**. Se viene generato un timestamp di trasmissione mentre il buffer è pieno, il nuovo timestamp viene eliminato.

**SO_TIMESTAMP_ID** (0x300B) è definito in `mstcpip.h` . È necessario fornire i dati del messaggio di controllo come **UINT32**.

I timestamp sono rappresentati come valore del contatore a 64 bit. La frequenza del contatore dipende dall'origine del timestamp. Per i timestamp software, il contatore è un [**valore QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) ed è possibile determinarne la frequenza [**tramite QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency). Per i timestamp hardware nic, la frequenza del contatore dipende dall'hardware della scheda di interfaccia di rete ed è possibile determinarla con informazioni aggiuntive fornite da [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp). Per determinare l'origine dei timestamp, usare le [**funzioni GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) e [**GetInterfaceSupportedTimestampCapabilities.**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)

Oltre alla configurazione a livello di socket usando l'opzione [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket per abilitare la ricezione di timestamp per un socket, è necessaria anche la configurazione a livello di sistema.

## <a name="estimating-latency-of-socket-send-path"></a>Stima della latenza del percorso di invio socket

In questa sezione verranno utilizzati timestamp di trasmissione per stimare la latenza del percorso di invio del socket. Se si dispone di un'applicazione esistente che utilizza timestamp di I/O a livello di applicazione in cui il timestamp deve essere il più vicino possibile al punto di trasmissione effettivo, questo esempio fornisce una descrizione quantitativa di quanto le API di timestamp Di Winsock possano migliorare l'accuratezza &mdash; &mdash; dell'applicazione.

L'esempio presuppone che nel sistema sia presente una sola scheda di interfaccia di rete (NIC) e che *interfaceLuid* sia il LUID di tale scheda.

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

## <a name="estimating-latency-of-socket-receive-path"></a>Stima della latenza del percorso di ricezione socket

Ecco un esempio simile per il percorso di ricezione. L'esempio presuppone che nel sistema sia presente una sola scheda di interfaccia di rete (NIC) e che *interfaceLuid* sia il LUID di tale scheda.

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

## <a name="a-limitation"></a>Una limitazione

Una limitazione delle API di timestamp di Winsock è che la chiamata SIO_GET_TX_TIMESTAMP [**è**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) sempre un'operazione non bloccante. Anche la chiamata di IOCTL in modalità OVERLAPPED comporta un ritorno immediato di **WSAEWOULDBLOCK** se non sono attualmente disponibili timestamp di trasmissione. Poiché i timestamp di trasmissione potrebbero non essere immediatamente disponibili dopo il ritorno di [**WSASendMsg,**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) l'applicazione deve eseguire il polling di IOCTL fino a quando il timestamp non è disponibile. È garantito che un timestamp di trasmissione sia disponibile dopo una chiamata **WSASendMsg** riuscita, dato che il buffer del timestamp di trasmissione non è pieno.
