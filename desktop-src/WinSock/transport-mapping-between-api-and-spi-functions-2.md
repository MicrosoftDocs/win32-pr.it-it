---
description: Il trasporto SPI di Winsock è simile all'API Winsock in quanto vengono visualizzate tutte le funzioni socket di base.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Mapping del trasporto tra le funzioni API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f11b950c48d0887f1e593c65f9d77e27c33917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315763"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Mapping del trasporto tra le funzioni API e SPI

Il trasporto SPI di Winsock è simile all'API Winsock in quanto vengono visualizzate tutte le funzioni socket di base. Quando nell'API sono presenti una nuova versione di una funzione Winsock e la versione originale, solo la nuova versione viene visualizzata in SPI. Questa operazione è illustrata nell'elenco seguente.

-   [**Connetti**](/windows/desktop/api/Winsock2/nf-winsock2-connect) e [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) entrambi mappati a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**accetta**](/windows/desktop/api/Winsock2/nf-winsock2-accept) e [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) mappa a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) mappato a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Altre funzioni API compresse nelle versioni avanzate di SPI includono:

-   [**Invia**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Le funzioni di supporto come [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)e [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) sono implementate nella \_32.dll WS2 e non vengono passate ai provider di servizi. Lo stesso vale per le versioni WSA di queste funzioni.

L'enumerazione del provider di servizi Windows Sockets e le funzioni correlate all'hook di blocco sono realizzate nel \_32.dll WS2, pertanto [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)e [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) non vengono visualizzate come funzioni SPI.

Poiché i codici di errore vengono restituiti insieme alle funzioni SPI, gli equivalenti di [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) e [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) non sono necessari in spi.

Le funzioni di manipolazione e attesa degli oggetti evento, tra cui [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , vengono mappate direttamente ai servizi Windows nativi e pertanto non sono presenti in spi.

Tutte le funzioni di conversione e risoluzione dei nomi specifiche di TCP/IP in Windows Sockets 1,1, ad esempio **GetXbyY**, **WSAAsyncGetXByY** e [**WSACancelAsyncRequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest), e [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) sono implementate all'interno \_ di WS232.dll in termini di nuove funzionalità di risoluzione dei nomi. Per ulteriori informazioni, vedere [risoluzione dei nomi compatibili per TCP/IP in Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Le funzioni di conversione come [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) e [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) vengono implementate all'interno di WS2 \_32.dll.

 

 
