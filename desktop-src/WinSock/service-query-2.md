---
description: Query del servizio dei nomi Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Query del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5452c94c3768cbff387b0125fe183a3026f7ab6c64d90325341ce5f2a9366de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740420"
---
# <a name="service-query"></a>Query del servizio

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Una query del servizio dei nomi include una serie di chiamate: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), seguita da una o più chiamate a [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) e terminano con una chiamata a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come input per definire i parametri di query insieme a un set di flag per fornire un controllo aggiuntivo sull'operazione di ricerca. Restituisce un handle di query usato nelle chiamate successive a **NSPLookupServiceNext** **e NSPLookupServiceEnd**.

Il client SPI dello spazio dei nomi richiama [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) per ottenere i risultati della query, con i risultati forniti in un buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornito dal client. Il client continua a chiamare **NSPLookupServiceNext** fino a quando non viene restituito il codice di errore WSA E NO MORE che indica che sono stati recuperati \_ tutti i \_ \_ risultati. La ricerca viene quindi terminata da una chiamata a [**NSPLookupServiceEnd.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend) La **funzione NSPLookupServiceEnd** può essere usata anche per annullare un **oggetto NSPLookupServiceNext** attualmente in sospeso quando viene chiamato da un altro thread.

In Windows Sockets 2, i codici di errore in conflitto sono definiti per WSAENOMORE (10102) e WSA \_ E \_ NO MORE \_ (10110). Il codice di errore WSAENOMORE verrà rimosso in una versione futura e rimarrà solo WSA \_ E \_ NO \_ MORE. I provider dello spazio dei nomi devono passare all'uso del codice di errore WSA E NO MORE appena possibile per mantenere la compatibilità con la \_ più ampia gamma possibile di \_ \_ applicazioni.

 

 



