---
description: Windows Sockets 2 fornisce un metodo generico per l'utilizzo delle funzionalità multipoint e multicast dei trasporti.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multicast e MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309945"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent multicast e MultiPoint

Windows Sockets 2 fornisce un metodo generico per l'utilizzo delle funzionalità multipoint e multicast dei trasporti. Questo metodo generico implementa queste funzionalità così come consente l'accesso alle funzionalità di trasporto dei dati di base di numerosi protocolli di trasporto. Il termine multipoint viene usato in seguito per fare riferimento alle comunicazioni multicast e MultiPoint.

Le implementazioni multipoint correnti (ad esempio, multicast IP, ST-II, T. 120 e ATM UNI) variano notevolmente. Il modo in cui i nodi vengono aggiunti a una sessione MultiPoint, se un determinato nodo viene designato come nodo centrale o radice e se i dati vengono scambiati tra tutti i nodi o solo tra un nodo radice e i vari nodi foglia sono diversi tra le implementazioni. La struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per Windows Sockets 2 viene usata per dichiarare i vari attributi MultiPoint di un protocollo. Esaminando questi attributi, il programmatore sa quali convenzioni seguire con le funzioni di Windows Sockets 2 applicabili per configurare, utilizzare e rimuovere le sessioni multipoint.

Di seguito sono riepilogate le funzionalità Winsock che supportano multipoint:

-   Bit a due attributi nella struttura [**di \_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quattro flag definiti per il parametro *dwFlags* della funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Una funzione, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), per l'aggiunta di nodi foglia in una sessione multipoint
-   Due codici di comando di [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per il controllo di loopback multipoint e la definizione dell'ambito per trasmissioni multicast. (Quest'ultimo corrisponde al parametro TTL (time-to-Live) del multicast IP.

> [!Note]  
> L'inclusione di queste funzionalità multipoint in Windows Sockets 2 non impedisce a un'applicazione di usare un'interfaccia dipendente dal protocollo esistente, ad esempio le opzioni dei socket di cervo per il multicast IP.

 

Vedere [semantica multipoint e multicast](multipoint-and-multicast-semantics-2.md) per informazioni dettagliate sul modo in cui vengono caratterizzati i diversi schemi multipoint e sulle modalità di utilizzo delle funzionalità applicabili di Windows Sockets 2.

 

 
