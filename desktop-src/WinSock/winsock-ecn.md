---
title: Notifica di congestione esplicita di Winsock (ECN)
description: Alcune applicazioni e/o protocolli basati sul protocollo UDP (User Datagram Protocol), ad esempio QUIC, cercano di sfruttare l'uso di punti di codice ECN (Explicit Congestion Notification) per migliorare la latenza e jitter nelle reti congestionate.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559972"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a><span data-ttu-id="4d622-103">Notifica di congestione esplicita di Winsock (ECN)</span><span class="sxs-lookup"><span data-stu-id="4d622-103">Winsock explicit congestion notification (ECN)</span></span>

## <a name="introduction"></a><span data-ttu-id="4d622-104">Introduzione</span><span class="sxs-lookup"><span data-stu-id="4d622-104">Introduction</span></span>

<span data-ttu-id="4d622-105">Alcune applicazioni e/o protocolli basati sul protocollo UDP (User Datagram Protocol), ad esempio QUIC, cercano di sfruttare l'uso di punti di codice ECN (Explicit Congestion Notification) per migliorare la latenza e jitter nelle reti congestionate.</span><span class="sxs-lookup"><span data-stu-id="4d622-105">Some applications and/or protocols that are based on the User Datagram Protocol (UDP) (for example, QUIC) seek to leverage the use of explicit congestion notification (ECN) codepoints in order to improve latency and jitter in congested networks.</span></span>

<span data-ttu-id="4d622-106">Le API ECN Winsock estendono l'interfaccia dei messaggi di controllo **getsockopt** / **setsockopt** e &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) con il supporto per la modifica e la ricezione di punti di codice ECN nelle intestazioni &mdash; IP.</span><span class="sxs-lookup"><span data-stu-id="4d622-106">The Winsock ECN APIs extend the **getsockopt**/**setsockopt** interface&mdash;as well as the [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)/[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) control message interface&mdash;with support for modifying and receiving ECN codepoints in IP headers.</span></span> <span data-ttu-id="4d622-107">La funzionalità fornita consente di ottenere e impostare punti di codice ECN in base al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4d622-107">The functionality provided allows you to get and set ECN codepoints on a per-packet basis.</span></span>

<span data-ttu-id="4d622-108">Per altre informazioni su ECN, vedere Aggiunta della notifica di congestione esplicita [(ECN) all'indirizzo IP.](https://tools.ietf.org/html/rfc3168)</span><span class="sxs-lookup"><span data-stu-id="4d622-108">For more information regarding ECN, see [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span></span>

<span data-ttu-id="4d622-109">L'applicazione non può specificare il punto di codice Congestion Encountered (CE) durante l'invio di datagrammi.</span><span class="sxs-lookup"><span data-stu-id="4d622-109">Your application isn't allowed to specify the Congestion Encountered (CE) code point when sending datagrams.</span></span> <span data-ttu-id="4d622-110">L'invio restituirà **l'errore WSAEINVAL**.</span><span class="sxs-lookup"><span data-stu-id="4d622-110">The send will return with error **WSAEINVAL**.</span></span>

## <a name="query-ecn-with-wsagetrecvipecn"></a><span data-ttu-id="4d622-111">Eseguire query ecn con WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="4d622-111">Query ECN with WSAGetRecvIPEcn</span></span>

<span data-ttu-id="4d622-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) è una funzione inline, definita in `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="4d622-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="4d622-113">Chiamare **WSAGetRecvIPEcn** per eseguire una query sull'abilitazione corrente della ricezione del messaggio di controllo **IP_ECN** (o **IPV6_ECN)** tramite [**LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)</span><span class="sxs-lookup"><span data-stu-id="4d622-113">Call **WSAGetRecvIPEcn** to query the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span></span>

<span data-ttu-id="4d622-114">Vedere anche la [**struttura WSAMSG.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)</span><span class="sxs-lookup"><span data-stu-id="4d622-114">Also see the [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) structure.</span></span>

- <span data-ttu-id="4d622-115">**Protocollo**: IPv4</span><span class="sxs-lookup"><span data-stu-id="4d622-115">**Protocol**: IPv4</span></span>
- <span data-ttu-id="4d622-116">**Cmsg_level**: IPPROTO_IP</span><span class="sxs-lookup"><span data-stu-id="4d622-116">**Cmsg_level**: IPPROTO_IP</span></span>
- <span data-ttu-id="4d622-117">**Cmsg_type**: IP_ECN (50 decimali)</span><span class="sxs-lookup"><span data-stu-id="4d622-117">**Cmsg_type**: IP_ECN (50 decimal)</span></span>
- <span data-ttu-id="4d622-118">**Descrizione:** specifica/riceve il punto di codice ECN nel campo di intestazione IPv4 Tipo di servizio (TOS).</span><span class="sxs-lookup"><span data-stu-id="4d622-118">**Description**: Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field.</span></span>

- <span data-ttu-id="4d622-119">**Protocollo**: IPv6</span><span class="sxs-lookup"><span data-stu-id="4d622-119">**Protocol**: IPv6</span></span>
- <span data-ttu-id="4d622-120">**Cmsg_level**: IPPROTO_IPV6</span><span class="sxs-lookup"><span data-stu-id="4d622-120">**Cmsg_level**: IPPROTO_IPV6</span></span>
- <span data-ttu-id="4d622-121">**Cmsg_type**: IPV6_ECN (50 decimali)</span><span class="sxs-lookup"><span data-stu-id="4d622-121">**Cmsg_type**: IPV6_ECN (50 decimal)</span></span>
- <span data-ttu-id="4d622-122">**Descrizione:** specifica/riceve il punto di codice ECN nel campo intestazione IPv6 della classe di traffico.</span><span class="sxs-lookup"><span data-stu-id="4d622-122">**Description**: Specifies/receives ECN codepoint in the Traffic Class IPv6 header field.</span></span>

## <a name="specify-ecn-with-wsasetrecvipecn"></a><span data-ttu-id="4d622-123">Specificare ECN con WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="4d622-123">Specify ECN with WSASetRecvIPEcn</span></span>

<span data-ttu-id="4d622-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) è una funzione inline, definita in `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="4d622-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="4d622-125">Chiamare **WSASetRecvIPEcn** per specificare se lo stack IP deve popolare il buffer di controllo con un messaggio contenente il punto di codice ECN del campo di intestazione Tipo di servizio IPv4 (o campo di intestazione IPv6 della classe di traffico) in un datagramma ricevuto.</span><span class="sxs-lookup"><span data-stu-id="4d622-125">Call **WSASetRecvIPEcn** to specify whether the IP stack should populate the control buffer with a message containing the ECN codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.</span></span> <span data-ttu-id="4d622-126">Se impostata su `TRUE` , la funzione LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce dati di controllo facoltativi contenenti il punto di codice ECN del datagramma ricevuto.</span><span class="sxs-lookup"><span data-stu-id="4d622-126">When set to `TRUE`, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram.</span></span> <span data-ttu-id="4d622-127">Il tipo di messaggio di controllo restituito **sarà IP_ECN** (o **IPV6_ECN**) con livello IPPROTO_IP **(o IPPROTO_IPV6**). </span><span class="sxs-lookup"><span data-stu-id="4d622-127">The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**).</span></span> <span data-ttu-id="4d622-128">I dati del messaggio di controllo vengono restituiti come **INT.**</span><span class="sxs-lookup"><span data-stu-id="4d622-128">The control message data is returned as an **INT**.</span></span> <span data-ttu-id="4d622-129">Questa opzione è valida solo nei socket di datagramma (il tipo di socket deve **essere SOCK_DGRAM**).</span><span class="sxs-lookup"><span data-stu-id="4d622-129">This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).</span></span>

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a><span data-ttu-id="4d622-130">Esempio di codice 1 &mdash; applicazione che pubblicizza il supporto ECN</span><span class="sxs-lookup"><span data-stu-id="4d622-130">Code example 1&mdash;application advertising ECN support</span></span>

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

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
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a><span data-ttu-id="4d622-131">Esempio di codice &mdash; 2: applicazione che rileva la congestione</span><span class="sxs-lookup"><span data-stu-id="4d622-131">Code example 2&mdash;application detecting congestion</span></span>

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a><span data-ttu-id="4d622-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d622-132">See also</span></span>

* [<span data-ttu-id="4d622-133">WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="4d622-133">WSAGetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [<span data-ttu-id="4d622-134">WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="4d622-134">WSASetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
