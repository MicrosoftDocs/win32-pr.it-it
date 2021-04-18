---
title: Differenze semantiche tra i socket multipoint e i socket normali
description: Differenze tra i \_ socket multipoint radice c e i socket da punto a punto regolari.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310438"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Differenze semantiche tra i socket multipoint e i socket normali

Nel piano di controllo sono presenti alcune differenze semantiche significative tra un \_ socket radice c e un socket Point-to-Point normale:

-   Il \_ socket radice c può essere usato in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per unire in join una nuova foglia.
-   L'inserimento di un \_ socket radice c in modalità di ascolto (chiamando [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) non impedisce che il \_ socket radice c venga usato in una chiamata a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere una nuova foglia o per l'invio e la ricezione di dati multipoint.
-   La chiusura di un \_ socket radice c causa la \_ notifica di chiusura FD a tutti i socket foglia c associati \_ .

Non esistono differenze semantiche tra un \_ socket foglia c e un socket normale nel piano di controllo, ad eccezione del fatto che il \_ socket foglia c può essere usato in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)e l'uso del \_ socket foglia c in [**ascolto**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indica che devono essere accettate solo le richieste di connessione multipoint.

Nel piano dati, le differenze semantiche tra il \_ socket radice d e un socket da punto a punto normale sono:

-   I dati inviati sul \_ socket radice d vengono recapitati a tutte le foglie nella stessa sessione multipoint.
-   I dati ricevuti nel \_ socket radice d possono provenire da una qualsiasi delle foglie.

Il \_ socket foglia d nel piano dati radice non presenta alcuna differenza semantica rispetto al socket normale. Tuttavia, nel piano dati non radice, i dati inviati sul \_ socket foglia d passano a tutti gli altri nodi foglia e i dati ricevuti possono provenire da qualsiasi altro nodo foglia. Come indicato in precedenza, le informazioni relative al fatto che il \_ socket foglia d si trovi in un piano dati radice o non radice è contenuto nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente per il socket.

 

 
