---
description: Supporto IPv6, allegato TCP/IP e Windows Socket.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Supporto IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f48e5b46ef1fcf1a2257db4a04b5435443552bb49f6c3c2b2dc4784077dcbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794801"
---
# <a name="ipv6-support"></a>Supporto IPv6

Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, uno da usare con IPv4 e un socket per l'uso con IPv6. Questi due socket devono essere gestiti separatamente dall'applicazione.

Se un provider di servizi TCP/IP in Windows XP con SP1 e in Windows Server 2003 supporta l'indirizzamento IPv4 e IPv6, deve creare due socket separati e restare in ascolto separatamente su questi socket:

-   Una volta per IPv4.
-   Una volta per la famiglia di indirizzi IPv6.

Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 in grado di gestire sia il traffico IPv6 che il traffico IPv4. Ad esempio, viene creato un socket di ascolto TCP per IPv6, viene attivata la modalità dual stack e viene associato alla porta 5001. Questo socket a doppio stack può accettare connessioni da client TCP IPv6 che si connettono alla porta 5001 e da client TCP IPv4 che si connettono alla porta 5001. Questa funzionalità consente di semplificare notevolmente la progettazione delle applicazioni e riduce il sovraccarico delle risorse necessario per la pubblicazione di operazioni su due socket separati. Esistono tuttavia alcune restrizioni che devono essere soddisfatte per usare un socket a doppio stack. Per altre informazioni, vedere [Dual-Stack Sockets](dual-stack-sockets.md).

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) restituisce due [**strutture WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per ognuno dei tipi di socket supportati (SOCK \_ STREAM, SOCK \_ DGRAM, SOCK \_ RAW). **iAddressFamily** deve essere impostato su AF INET per l'indirizzamento IPv4 e su \_ AF \_ INET6 per l'indirizzamento IPv6.

Gli indirizzi IPv6 sono descritti nelle strutture seguenti.

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

Se un'applicazione usa funzioni Windows Sockets 1.1 e vuole usare indirizzi IPv6, può continuare a usare tutte le funzioni vecchie che accettano la struttura [**sockaddr**](sockaddr-2.md) come uno dei parametri ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)e così via). L'unica modifica necessaria è usare **sockaddr \_ in6** anziché **sockaddr \_ in**.

Tuttavia, le funzioni di risoluzione dei nomi ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e così via) e le funzioni di conversione degli indirizzi ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) non possono essere riutilizzate perché presuppongono che un indirizzo IP sia di 4 byte. Un'applicazione che vuole eseguire la risoluzione dei nomi e la conversione degli indirizzi per gli indirizzi IPv6 deve usare Windows specifiche di Sockets 2. Sono state introdotte molte nuove funzioni per consentire alle applicazioni Windows Sockets 2 di sfruttare IPv6, incluse le funzioni [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)

Per altre informazioni su come abilitare le funzionalità IPv6 in un'applicazione, vedere la guida [IPv6 per](ipv6-guide-for-windows-sockets-applications-2.md)applicazioni Windows Sockets .

 

 
