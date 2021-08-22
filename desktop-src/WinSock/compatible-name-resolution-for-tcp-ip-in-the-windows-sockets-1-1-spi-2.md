---
description: Windows I socket 1.1 hanno definito una serie di routine usate per la risoluzione dei nomi IPv4 con reti TCP/IP. Queste sono chiamate in modo personalizzato le funzioni GetXbyY e includono quanto segue.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Risoluzione dei nomi compatibile per TCP/IP in Windows Sockets 1.1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea355eb85d41a507e4970bf0c8d925a41ed81ca51c08b9c77955ad702a62d27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051679"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Risoluzione dei nomi compatibile per TCP/IP in Windows Sockets 1.1 SPI

Windows I socket 1.1 hanno definito una serie di routine usate per la risoluzione dei nomi IPv4 con reti TCP/IP. Queste sono chiamate in modo personalizzato le **funzioni GetXbyY** e includono quanto segue.

[**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

Sono state definite anche le versioni asincrone di queste funzioni.

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Queste funzioni sono specifiche delle reti TCP/IP. Gli sviluppatori di applicazioni indipendenti dal protocollo non sono sconsigliati di continuare a utilizzare queste funzioni specifiche del trasporto. Tuttavia, per mantenere la rigida compatibilità con le versioni precedenti di Windows Sockets 1.1, le funzioni precedenti continuano a essere supportate finché è presente almeno un provider dello spazio dei nomi che supporta la famiglia di indirizzi \_ AF INET.

Il32.dll *Ws2 \_* implementa queste funzioni di compatibilità in termini di nuove funzionalità di risoluzione dei nomi indipendenti dal protocollo usando una sequenza appropriata di chiamate di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) Di seguito vengono fornite informazioni dettagliate sul mapping delle funzioni **GetXbyY** alle funzioni di risoluzione dei nomi. Il32.dll Ws2 gestisce le differenze tra le versioni asincrone e sincrone delle funzioni GetXbyY, in modo da illustrare solo l'implementazione delle funzioni \_ **Sincrone GetXbyY.** 

 

 
