---
description: Differenze tra i socket Point-to-Point regolari e \_ i socket multipoint radice c in Windows Sockets (Winsock) SPI.
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Differenze semantiche tra i socket multipoint e i socket normali in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309934"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Differenze semantiche tra i socket multipoint e i socket normali in SPI

Nel piano di controllo sono presenti alcune differenze semantiche significative tra un \_ socket radice c e un socket Point-to-Point normale:

-   Il \_ socket radice c può essere usato in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per aggiungere una nuova foglia.
-   L'inserimento di un \_ socket radice c in modalità di ascolto (chiamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) non impedisce che il \_ socket radice c venga utilizzato in una chiamata a [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per aggiungere una nuova foglia o per l'invio e la ricezione di dati multipoint.
-   La chiusura di un socket radice c provocherà \_ la \_ notifica di chiusura FD a tutti i socket foglia c associati \_ .

Non esistono differenze semantiche tra un \_ socket foglia c e un socket normale nel piano di controllo, ad eccezione del fatto che il \_ socket foglia c può essere usato in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)e l'uso del \_ socket foglia c in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica che devono essere accettate solo le richieste di connessione multipoint.

Nel piano dati, le differenze semantiche tra il \_ socket radice d e un socket da punto a punto normale sono

-   I dati inviati nel \_ socket radice d verranno recapitati a tutte le foglie nella stessa sessione multipoint.
-   I dati ricevuti nel \_ socket radice d possono provenire da una qualsiasi delle foglie.

Il \_ socket foglia d nel piano dati radice non presenta alcuna differenza semantica rispetto al socket normale. Tuttavia, nel piano dati non radice, i dati inviati sul socket foglia d andranno \_ a tutti gli altri nodi foglia e i dati ricevuti potrebbero provenire da qualsiasi altro nodo foglia. Come indicato in precedenza, le informazioni relative al fatto che il \_ socket foglia d si trovi in un piano dati radice o non radice è contenuto nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente per il socket.

 

 
