---
description: Si noti che tutte le funzioni di Windows Sockets 1,1 per la risoluzione dei nomi sono specifiche delle reti TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307017"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1

> [!Note]  
> Tutte le funzioni di Windows Sockets 1,1 per la risoluzione dei nomi sono specifiche delle reti TCP/IP IPv4. Gli sviluppatori di applicazioni sono fortemente sconsigliati di continuare a utilizzare queste funzioni specifiche del trasporto che supportano solo IPv4.

 

Gli sviluppatori di applicazioni devono usare le funzioni seguenti che sono indipendenti dal protocollo e supportano sia la risoluzione dei nomi IPv6 che quella IPv4.

-   [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Sockets 1,1 definisce un numero di routine utilizzate per la risoluzione dei nomi con reti TCP/IP (IP versione 4). Queste sono talvolta chiamate funzioni **getXbyY** e includono quanto segue:

<dl>

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

Sono state definite anche le versioni asincrone di queste funzioni.

<dl>

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

Sono inoltre disponibili due funzioni, ora implementate nella Winsock2.dll, utilizzate per convertire rispettivamente la notazione degli indirizzi IPv4 punteggiata da e verso le rappresentazioni binarie e di stringa.

<dl>

[**\_indirizzo inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**\_NTOA inet**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

Per mantenere rigorosa la compatibilità con le versioni precedenti di Windows Sockets 1,1, tutte le funzioni solo IPv4 precedenti continuano a essere supportate purché sia presente almeno un provider dello spazio dei nomi che supporta la \_ famiglia di indirizzi AF inet (queste funzioni non sono rilevanti per IP versione 6, indicata da AF \_ INET6).

Il \_32.dll WS2 implementa queste funzioni di compatibilità in termini di nuove funzionalità di risoluzione dei nomi indipendenti dal protocollo usando una sequenza appropriata di chiamate di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **end** . Di seguito sono riportati i dettagli relativi alla modalità di mapping delle funzioni **getXbyY** alle funzioni di risoluzione dei nomi. WSs2 \_32.dll gestisce le differenze tra le versioni asincrone e sincrone delle funzioni **getXbyY** , in modo che venga discussa solo l'implementazione delle funzioni **getXbyY** sincrone.

In questa sezione viene descritta la risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1. Nell'elenco seguente vengono descritti gli argomenti di questa sezione:

-   [Approccio di base per GetXbyY nell'API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Funzioni getprotobyname e getprotobynumber nell'API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Funzioni getservbyname e getservbyport nell'API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Funzione gethostbyname nell'API](gethostbyname-function-in-the-api-2.md)
-   [Funzione gethostbyaddr nell'API](gethostbyaddr-function-in-the-api-2.md)
-   [Funzione GetHostName nell'API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
