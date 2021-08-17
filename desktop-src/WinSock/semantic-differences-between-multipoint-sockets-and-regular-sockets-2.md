---
title: Differenze semantiche tra socket multipoint e socket regolari
description: Differenze tra i socket multipoint radice c e i normali socket da punto \_ a punto.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b30ff05c72fc43bf3f4e731242d9f22a2236e9f6fd275c382b57fb05d094cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740811"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Differenze semantiche tra socket multipoint e socket regolari

Nel piano di controllo esistono alcune differenze semantiche significative tra un socket radice c e un normale socket da punto \_ a punto:

-   Il socket radice c \_ può essere usato in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per unire una nuova foglia.
-   L'inserimento di un socket radice c in modalità di ascolto (chiamando listen ) non preclude l'uso del socket radice c in una chiamata \_ [](/windows/desktop/api/Winsock2/nf-winsock2-listen) \_ a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere una nuova foglia o per l'invio e la ricezione di dati multipunto.
-   La chiusura di un socket radice c \_ fa sì che tutti i socket foglia c associati \_ otterrà la notifica FD \_ CLOSE.

Non esistono differenze semantiche tra un socket foglia c e un socket regolare nel piano di controllo, ad eccezione del fatto che il socket foglia c può essere usato \_ \_ in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)e l'uso di c leaf socket in listen indica che devono essere accettate solo le richieste di connessione \_ multipoint. [](/windows/desktop/api/Winsock2/nf-winsock2-listen)

Nel piano dati, le differenze semantiche tra il socket radice d e un normale socket da punto \_ a punto sono:

-   I dati inviati sul socket radice d \_ vengono recapitati a tutte le foglia nella stessa sessione multipunto.
-   I dati ricevuti nel socket radice d \_ possono essere provenienti da una delle foglia.

Il socket foglia d nel piano dati rooted non ha alcuna differenza semantica dal socket normale, tuttavia, nel piano dati non rooted, i dati inviati sul socket foglia d passano a tutti gli altri nodi foglia e i dati ricevuti potrebbero essere provenienti da qualsiasi altro nodo \_ \_ foglia. Come accennato in precedenza, le informazioni sul fatto che il socket foglia d si trova in un piano dati rooted o nonrooted è contenuto nella struttura \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente per il socket.

 

 
