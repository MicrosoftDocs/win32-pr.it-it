---
description: Windows Socket (Winsock) e funzionalità multipoint e multicast indipendenti dal protocollo dei trasporti.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent Multicast e Multipoint nello SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f6e7176d9b64ac8c7ef339ee82b8252e2a0d466dd8709fa008363ec3ef954e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993621"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent Multicast e Multipoint nello SPI

Così come Windows Sockets 2 consente l'accesso generico alle funzionalità di trasporto dati di base di numerosi protocolli di trasporto, offre anche un modo generico per usare le funzionalità multipoint e multicast dei trasporti che implementano queste funzionalità. Per semplificare, il termine *multipoint* viene usato successivamente per fare riferimento alle comunicazioni multicast e multipoint.

Le attuali implementazioni multipoint (ad esempio, multicast IP, ST-II, T.120, ATM UNI) variano notevolmente in relazione al modo in cui i nodi si uniscono a una sessione multipoint, se un determinato nodo è designato come nodo centrale o radice e se i dati vengono smesti tra tutti i nodi o solo tra un nodo radice e vari nodi foglia. La Windows [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) di Sockets 2 viene usata per dichiarare gli attributi multipoint di un protocollo. Esaminando questi attributi, il programmatore saprà quali convenzioni seguire nell'uso delle funzioni Winsock applicabili per configurare, usare e disaccontire le sessioni multipoint.

Le funzionalità di Windows Sockets 2 che supportano il multicast possono essere riepilogate nel modo seguente:

-   Tre bit di attributo nella [**struttura WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Quattro flag definiti per il *parametro dwFlags* di [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Una funzione, [**WSPJoinLeaf,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)per l'aggiunta di nodi foglia in una sessione multipoint.
-   Due [**codici di comando WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) per il controllo del loopback multipoint e la definizione dell'ambito per le trasmissioni multicast. Quest'ultimo corrisponde al parametro time-to-live o TTL multicast IP.

> [!Note]  
> L'inclusione di queste funzionalità multipoint in Windows Sockets 2 non preclude a un provider di servizi di supportare anche un'interfaccia dipendente dal protocollo esistente, ad esempio le opzioni socket di deering per il multicast IP.

 

 

 
