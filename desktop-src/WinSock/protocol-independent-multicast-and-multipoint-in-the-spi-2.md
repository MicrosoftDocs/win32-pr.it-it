---
description: Windows Sockets (Winsock) e funzionalità multipoint e multicast indipendenti dal protocollo dei trasporti.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multicast e MultiPoint in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131175"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent multicast e MultiPoint in SPI

Così come Windows Sockets 2 consente di accedere alle funzionalità di base di trasporto dei dati di numerosi protocolli di trasporto in modo generico, fornisce anche un modo generico per usare le funzionalità multipoint e multicast dei trasporti che implementano queste funzionalità. Per semplificare, il termine *multipoint* viene usato in seguito per fare riferimento alle comunicazioni multicast e MultiPoint.

Le implementazioni multipoint correnti (ad esempio, multicast IP, ST-II, T. 120, ATM UNI) variano notevolmente in base al modo in cui i nodi si uniscono a una sessione MultiPoint, a seconda che un determinato nodo sia designato come nodo centrale o radice e che i dati vengano scambiati tra tutti i nodi o solo tra un nodo radice e vari nodi foglia. La struttura delle [**\_ informazioni**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) di Windows Sockets 2 WSAPROTOCOL viene usata per dichiarare gli attributi MultiPoint di un protocollo. Esaminando questi attributi, il programmatore saprà le convenzioni da seguire per l'uso delle funzioni Winsock applicabili per configurare, usare e rimuovere le sessioni multipoint.

Le funzionalità di Windows Sockets 2 che supportano il multicast possono essere riepilogate come segue:

-   Tre bit di attributo nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quattro flag definiti per il parametro *dwFlags* di [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Una funzione, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), per l'aggiunta di nodi foglia in una sessione multipoint.
-   Due codici di comando di [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) per il controllo di loopback multipoint e la definizione dell'ambito per trasmissioni multicast. (Quest'ultimo corrisponde al parametro TTL (time-to-Live) del multicast IP.

> [!Note]  
> L'inclusione di queste funzionalità multipoint in Windows Sockets 2 non impedisce a un provider di servizi di supportare anche un'interfaccia dipendente dal protocollo esistente, ad esempio le opzioni socket di Deering per il multicast IP.

 

 

 
