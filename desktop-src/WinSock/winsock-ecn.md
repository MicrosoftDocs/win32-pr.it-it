---
title: Notifica esplicita di congestione (ECN) di Winsock
description: Alcune applicazioni e/o protocolli basati sul protocollo UDP (User Datagram Protocol), ad esempio QUIC, cercano di sfruttare l'uso di punti di codice ECN (Explicit Congestion Notification) per migliorare la latenza e instabilità nelle reti congestionate.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 79b38611cd0301d0b5d301592eec02b68c02353246c67a6c94528417623834f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322024"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a>Notifica esplicita di congestione (ECN) di Winsock

## <a name="introduction"></a>Introduzione

Alcune applicazioni e/o protocolli basati sul protocollo UDP (User Datagram Protocol), ad esempio QUIC, cercano di sfruttare l'uso di punti di codice ECN (Explicit Congestion Notification) per migliorare la latenza e instabilità nelle reti congestionate.

Le API ECN Winsock estendono l'interfaccia dei messaggi di controllo **getsockopt** / **setsockopt** e &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) con il supporto per la modifica e la ricezione di punti di codice ECN nelle intestazioni &mdash; IP. La funzionalità fornita consente di ottenere e impostare punti di codice ECN in base al pacchetto.

Per altre informazioni su ECN, vedere The Addition of Explicit Congestion Notification (ECN) to IP ( Aggiunta della notifica di congestione esplicita [(ECN) all'INDIRIZZO IP).](https://tools.ietf.org/html/rfc3168)

L'applicazione non può specificare il punto di codice Congestion Encountered (CE) durante l'invio di datagrammi. L'invio restituirà **l'errore WSAEINVAL**.

## <a name="query-ecn-with-wsagetrecvipecn"></a>Eseguire query ECN con WSAGetRecvIPEcn

[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) è una funzione inline, definita in `ws2tcpip.h` .

Chiamare **WSAGetRecvIPEcn** per eseguire una query sull'abilitazione corrente della ricezione del messaggio di controllo **IP_ECN** (o **IPV6_ECN)** tramite [**LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

Vedere anche la [**struttura WSAMSG.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)

- **Protocollo:** IPv4
- **Cmsg_level**: IPPROTO_IP
- **Cmsg_type**: IP_ECN (50 decimali)
- **Descrizione:** specifica/riceve il punto di codice ECN nel campo di intestazione IPv4 Tipo di servizio (TOS).

- **Protocollo:** IPv6
- **Cmsg_level**: IPPROTO_IPV6
- **Cmsg_type**: IPV6_ECN (50 decimali)
- **Descrizione:** specifica/riceve il punto di codice ECN nel campo intestazione IPv6 della classe di traffico.

## <a name="specify-ecn-with-wsasetrecvipecn"></a>Specificare ECN con WSASetRecvIPEcn

[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) è una funzione inline, definita in `ws2tcpip.h` .

Chiamare **WSASetRecvIPEcn** per specificare se lo stack IP deve popolare il buffer di controllo con un messaggio contenente il punto di codice ECN del campo di intestazione Tipo di servizio IPv4 (o campo di intestazione IPv6 della classe di traffico) in un datagramma ricevuto. Se impostata su `TRUE` , la funzione LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce dati di controllo facoltativi contenenti il punto di codice ECN del datagramma ricevuto. Il tipo di messaggio di controllo restituito **sarà IP_ECN** (o **IPV6_ECN**) con livello IPPROTO_IP **(o IPPROTO_IPV6**).  I dati del messaggio di controllo vengono restituiti come **INT.** Questa opzione è valida solo nei socket di datagramma (il tipo di socket deve **essere SOCK_DGRAM**).

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>Esempio di codice 1 &mdash; applicazione che pubblicizza il supporto ECN

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

## <a name="code-example-2mdashapplication-detecting-congestion"></a>Esempio di codice &mdash; 2: applicazione che rileva la congestione

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

## <a name="see-also"></a>Vedi anche

* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
