---
description: Windows Sockets 2 fornisce un metodo generico per l'utilizzo delle funzionalità multipoint e multicast dei trasporti.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent Multicast e Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238949f017c2ecb910b533d12a809aa1c04af02e64d08aa0ef4e8d4f3d39b71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857904"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent Multicast e Multipoint

Windows Sockets 2 fornisce un metodo generico per l'utilizzo delle funzionalità multipoint e multicast dei trasporti. Questo metodo generico implementa queste funzionalità proprio come consente l'accesso alle funzionalità di trasporto dati di base di numerosi protocolli di trasporto. Il termine multipoint viene usato successivamente per fare riferimento alle comunicazioni multicast e multipoint.

Le attuali implementazioni multipoint (ad esempio, multicast IP, ST-II, T.120 e ATM UNI) variano notevolmente. Il modo in cui i nodi si uniscono a una sessione multipoint, se un determinato nodo è designato come nodo centrale o radice e se i dati vengono s scambiati tra tutti i nodi o solo tra un nodo radice e i vari nodi foglia differiscono tra le implementazioni. La [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per Windows Sockets 2 viene usata per dichiarare i vari attributi multipoint di un protocollo. Esaminando questi attributi, il programmatore conosce le convenzioni da seguire con le funzioni Windows Sockets 2 applicabili per configurare, usare ed eseguire l'downing di sessioni multipoint.

Di seguito sono riepilogate le funzionalità di Winsock che supportano multipoint:

-   Bit a due attributi nella [**struttura WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Quattro flag definiti per il *parametro dwFlags* della [**funzione WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
-   Una funzione, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)per l'aggiunta di nodi foglia in una sessione multipoint
-   Due [**codici di comando WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per il controllo del loopback multipoint e la definizione dell'ambito per le trasmissioni multicast. Quest'ultimo corrisponde al parametro time-to-live o TTL multicast IP.

> [!Note]  
> L'inclusione di queste funzionalità multipoint in Windows Sockets 2 non preclude a un'applicazione di usare un'interfaccia esistente dipendente dal protocollo, ad esempio le opzioni socket di deering per il multicast IP.

 

Vedere [Semantica multipoint](multipoint-and-multicast-semantics-2.md) e multicast per informazioni dettagliate su come sono caratterizzati i vari schemi multipoint e su come vengono utilizzate le funzionalità applicabili di Windows Sockets 2.

 

 
