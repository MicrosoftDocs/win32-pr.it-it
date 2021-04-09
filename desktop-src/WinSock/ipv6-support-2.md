---
description: Supporto IPv6, allegati TCP/IP e Windows Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Supporto IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129167"
---
# <a name="ipv6-support"></a>Supporto IPv6

Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, un socket da usare con IPv4 e un socket per l'uso con IPv6. Questi due socket devono essere gestiti separatamente dall'applicazione.

Se un provider di servizi TCP/IP in Windows XP con SP1 e in Windows Server 2003 supporta l'indirizzamento IPv4 e IPv6, deve creare due socket distinti e restare in ascolto separatamente su questi socket:

-   Una volta per IPv4.
-   Una volta per la famiglia di indirizzi IPv6.

Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 che può gestire sia il traffico IPv6 che quello IPv4. Ad esempio, viene creato un socket di ascolto TCP per IPv6, inserito in modalità dual stack e associato alla porta 5001. Questo socket a doppio stack può accettare connessioni da client TCP IPv6 che si connettono alla porta 5001 e dai client TCP IPv4 che si connettono alla porta 5001. Questa funzionalità consente di semplificare notevolmente la progettazione delle applicazioni e riduce il sovraccarico delle risorse richiesto per l'invio di operazioni su due socket distinti. Tuttavia, esistono alcune restrizioni che devono essere soddisfatte per poter utilizzare un socket a doppio stack. Per altre informazioni, vedere [socket a doppio stack](dual-stack-sockets.md).

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) restituisce due strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per ognuno dei tipi di socket supportati (Sock \_ Stream, Sock \_ DGRAM, Sock \_ RAW). **IAddressFamily** deve essere impostato su AF \_ inet per l'indirizzamento IPv4 e su AF \_ INET6 per l'indirizzamento IPv6.

Gli indirizzi IPv6 sono descritti nelle seguenti strutture.

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

Se un'applicazione usa le funzioni di Windows Sockets 1,1 e vuole usare gli indirizzi IPv6, può continuare a usare tutte le funzioni precedenti che accettano la struttura [**sockaddr**](sockaddr-2.md) come uno dei parametri ([**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)e così via). L'unica modifica necessaria consiste nell'usare **sockaddr \_ IN6** anziché **sockaddr \_ in**.

Tuttavia, le funzioni di risoluzione dei nomi ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e così via) e le funzioni di conversione degli indirizzi ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) non possono essere riutilizzate perché presuppongono che un indirizzo IP sia lungo 4 byte. Un'applicazione che vuole eseguire la risoluzione dei nomi e la conversione degli indirizzi per gli indirizzi IPv6 deve usare funzioni specifiche di Windows Sockets 2. Sono state introdotte molte nuove funzioni per consentire alle applicazioni Windows Sockets 2 di sfruttare i vantaggi di IPv6, incluse le funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Per ulteriori informazioni su come abilitare le funzionalità IPv6 in un'applicazione, vedere la [Guida IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
