---
description: Differenze tra i socket da punto a punto normali e i socket multipoint radice c \_ nell'interfaccia SPI Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Differenze semantiche tra i socket multipoint e i socket regolari in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e585c335d7503d884d58e25b6fc0ad6dd0c0c3356064ebb1504898770d4b7b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740609"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Differenze semantiche tra i socket multipoint e i socket regolari in SPI

Nel piano di controllo esistono alcune differenze semantiche significative tra un socket radice c e un normale socket da punto \_ a punto:

-   Il socket radice c \_ può essere usato in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per creare un join di una nuova foglia.
-   L'inserimento di un socket radice c in modalità di ascolto (chiamando WSPListen ) non preclude l'uso del socket radice c in una chiamata \_ [](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) \_ a [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per aggiungere una nuova foglia o per l'invio e la ricezione di dati multipunto.
-   La chiusura di un socket radice c causerà la notifica FD CLOSE di tutti i \_ socket foglia c \_ \_ associati.

Non esistono differenze semantiche tra un socket foglia c e un socket regolare nel piano di controllo, ad eccezione del fatto che il socket foglia c può essere usato \_ \_ in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)e l'uso del socket foglia c \_ in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica che devono essere accettate solo le richieste di connessione multipoint.

Nel piano dati le differenze semantiche tra il socket radice d e un normale socket da punto \_ a punto sono

-   I dati inviati sul socket radice d \_ verranno recapitati a tutte le foglia nella stessa sessione multipunto.
-   I dati ricevuti nel socket radice d \_ possono essere provenienti da una delle foglia.

Il socket foglia d nel piano dati rooted non ha alcuna differenza semantica dal socket normale, tuttavia nel piano dati non rooted i dati inviati sul socket foglia d verranno inviati a tutti gli altri nodi foglia e i dati ricevuti potrebbero essere provenienti da qualsiasi altro nodo \_ \_ foglia. Come accennato in precedenza, le informazioni sul fatto che il socket foglia d si trova in un piano dati rooted o nonrooted è contenuto nella struttura \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente per il socket.

 

 
