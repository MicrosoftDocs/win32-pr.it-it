---
description: Nota Tutte le funzioni Windows Sockets 1.1 per la risoluzione dei nomi sono specifiche delle reti TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13dfb1a403f782d0349e20729117fe1f4aed01479b01a6c2b5968f1d9bf15f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322301"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1

> [!Note]  
> Tutte le funzioni Windows Sockets 1.1 per la risoluzione dei nomi sono specifiche delle reti TCP/IP IPv4. Gli sviluppatori di applicazioni sono fortemente sconsigliati di continuare a usare queste funzioni specifiche del trasporto che supportano solo IPv4.

 

Gli sviluppatori di applicazioni devono usare le funzioni seguenti indipendenti dal protocollo e che supportano sia la risoluzione dei nomi IPv6 che IPv4.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Sockets 1.1 ha definito una serie di routine usate per la risoluzione dei nomi con reti TCP/IP (IP versione 4). Queste funzioni vengono talvolta chiamate **funzioni getXbyY** e includono quanto segue:

<dl>

[**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
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

Sono anche disponibili due funzioni, ora implementate nel Winsock2.dll, usate per convertire rispettivamente la notazione dell'indirizzo Ipv4 punteggiata in e da rappresentazioni stringa e binarie.

<dl>

[**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

Per mantenere la rigida compatibilità con le versioni precedenti con Windows Sockets 1.1, tutte le funzioni precedenti solo IPv4 continuano a essere supportate purché sia presente almeno un provider di spazi dei nomi che supporta la famiglia di indirizzi AF INET (queste funzioni non sono rilevanti per IP versione 6, indicato da \_ AF \_ INET6).

L'32.dll Ws2 implementa queste funzioni di compatibilità in termini di nuove funzionalità di risoluzione dei nomi indipendenti dal protocollo usando una sequenza appropriata di chiamate di funzione \_ [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End.** Di seguito sono riportati i dettagli del mapping delle funzioni **getXbyY** alle funzioni di risoluzione dei nomi. Il32.dll WSs2 gestisce le differenze tra le versioni asincrone e sincrone delle funzioni getXbyY, quindi viene illustrata solo l'implementazione delle funzioni \_ **getXbyY sincrone.** 

Questa sezione descrive la risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1. L'elenco seguente descrive gli argomenti di questa sezione:

-   [Approccio di base per GetXbyY nell'API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Funzioni getprotobyname e getprotobynumber nell'API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Funzioni getservbyname e getservbyport nell'API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Funzione gethostbyname nell'API](gethostbyname-function-in-the-api-2.md)
-   [Funzione gethostbyaddr nell'API](gethostbyaddr-function-in-the-api-2.md)
-   [Funzione gethostname nell'API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
