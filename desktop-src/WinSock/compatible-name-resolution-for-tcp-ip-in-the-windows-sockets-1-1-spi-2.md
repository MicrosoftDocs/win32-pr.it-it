---
description: Windows Sockets 1,1 definisce un numero di routine utilizzate per la risoluzione dei nomi IPv4 con le reti TCP/IP. Queste sono comunemente chiamate funzioni GetXbyY e includono quanto segue.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Risoluzione dei nomi compatibile per TCP/IP in Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307015"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Risoluzione dei nomi compatibile per TCP/IP in Windows Sockets 1,1 SPI

Windows Sockets 1,1 definisce un numero di routine utilizzate per la risoluzione dei nomi IPv4 con le reti TCP/IP. Queste sono comunemente chiamate funzioni **GetXbyY** e includono quanto segue.

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)

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

Queste funzioni sono specifiche delle reti TCP/IP; gli sviluppatori di applicazioni indipendenti dal protocollo sono sconsigliati di continuare a utilizzare queste funzioni specifiche del trasporto. Tuttavia, per mantenere rigorosa la compatibilità con le versioni precedenti di Windows Sockets 1,1, le funzioni precedenti continuano a essere supportate purché sia presente almeno un provider dello spazio dei nomi che supporta la \_ famiglia di indirizzi AF inet.

Il *\_32.dllWS2* implementa queste funzioni di compatibilità in termini di nuove funzionalità di risoluzione dei nomi indipendenti dal protocollo usando una sequenza appropriata di chiamate di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . Di seguito sono riportati i dettagli relativi alla modalità di mapping delle funzioni **GetXbyY** alle funzioni di risoluzione dei nomi. Il \_32.dll WS2 gestisce le differenze tra le versioni asincrone e sincrone delle funzioni **GetXbyY** , in modo che venga discussa solo l'implementazione delle funzioni **GetXbyY** sincrone.

 

 
