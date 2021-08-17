---
description: Winsock Transport SPI è simile all'API Winsock in cui vengono visualizzate tutte le funzioni socket di base.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Mapping del trasporto tra funzioni API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf4167353fa05c5656c588a9dff99c96564a5202ffdc4d21edf358c340634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739941"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Mapping del trasporto tra funzioni API e SPI

Winsock Transport SPI è simile all'API Winsock in cui vengono visualizzate tutte le funzioni socket di base. Quando nell'API sono presenti una nuova versione di una funzione Winsock e la versione originale, solo la nuova versione verrà mostrata in SPI. Questa operazione è illustrata nell'elenco seguente.

-   [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) e [**WSAConnect e**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) mappano entrambi a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) e [**mapping WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**Mapping di socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) [**e WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) [**a WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Altre funzioni API compresse nelle versioni avanzate in SPI includono:

-   [**Invia**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**Recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Le funzioni di supporto come [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl) [**e ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) vengono implementate nel32.dll Ws2 e non vengono passate ai provider \_ di servizi. Lo stesso vale per le versioni WSA di queste funzioni.

Windows L'enumerazione del provider di servizi Sockets e le funzioni correlate all'hook di blocco vengono realizzati nel32.dll Ws2, pertanto \_ [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)e [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) non vengono visualizzati come funzioni SPI.

Poiché i codici di errore vengono restituiti insieme alle funzioni SPI, gli equivalenti di [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) e [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) non sono necessari in SPI.

Le funzioni di modifica e attesa degli oggetti evento, tra cui [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents,**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) vengono mappate direttamente ai servizi Windows nativi e pertanto non sono presenti nell'interfaccia SPI.

Tutte le funzioni di conversione e risoluzione dei nomi specifiche di TCP/IP in Windows Sockets 1.1, ad esempio **GetXbyY**, **WSAAsyncGetXByY** e [**WSACancelAsyncRequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest), nonché [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) vengono implementate all'interno del32.dll Ws2 in termini di nuove funzionalità di risoluzione dei \_ nomi. Per altre informazioni, vedere Risoluzione dei nomi [compatibile per TCP/IP in Windows Sockets 1.1 SPI.](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md) Le funzioni di [**conversione, ad esempio inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) e [**inet \_ ntoa,**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) vengono implementate all'interno del32.dll Ws2. \_

 

 
