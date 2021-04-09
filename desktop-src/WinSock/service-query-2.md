---
description: Nome della query del servizio in Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Query del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049818"
---
# <a name="service-query"></a>Query del servizio

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Una query del servizio del nome include una serie di chiamate: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), seguite da una o più chiamate a [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) e che terminano con una chiamata a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come input per definire i parametri di query insieme a un set di flag per fornire un controllo aggiuntivo sull'operazione di ricerca. Restituisce un handle di query che viene usato nelle chiamate successive a **NSPLookupServiceNext** e **NSPLookupServiceEnd**.

Il client SPI dello spazio dei nomi richiama [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) per ottenere i risultati della query, con i risultati forniti in un buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornito dal client. Il client continua a chiamare **NSPLookupServiceNext** fino a quando non viene restituito il codice di errore WSA \_ E \_ , a \_ indicare che tutti i risultati sono stati recuperati. La ricerca viene quindi terminata da una chiamata a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). La funzione **NSPLookupServiceEnd** può essere usata anche per annullare un **NSPLookupServiceNext** attualmente in sospeso quando viene chiamato da un altro thread.

In Windows Sockets 2, i codici di errore in conflitto vengono definiti per WSAENOMORE (10102) e WSA \_ e \_ non \_ più (10110). Il codice di errore WSAENOMORE verrà rimosso in una versione futura e solo WSA \_ e \_ non \_ rimarrà più. \_ \_ \_ Per mantenere la compatibilità con la più ampia gamma possibile di applicazioni, i provider dello spazio dei nomi devono passare all'utilizzo della WSA E non più il codice di errore appena possibile.

 

 



