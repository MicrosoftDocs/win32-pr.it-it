---
description: L'helper IP fornisce funzionalità per la gestione delle schede di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gestione delle schede di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525891"
---
# <a name="managing-network-adapters"></a>Gestione delle schede di rete

L'helper IP fornisce funzionalità per la gestione delle schede di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.

Utilizzare le funzioni descritte nei paragrafi seguenti per recuperare informazioni sulle schede di rete nel computer locale.

La funzione [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) restituisce una matrice di strutture di [**\_ \_ informazioni della scheda IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , una per ogni scheda nel computer locale. La funzione [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) restituisce informazioni aggiuntive su un adapter specifico. La funzione **GetPerAdapterInfo** richiede che il chiamante specifichi l'indice dell'adapter. Per ottenere l'indice dell'adapter dal nome dell'adapter, utilizzare la funzione [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .

Alcune applicazioni utilizzano Adapter che ricevono datagrammi, ma non possono trasmetterli. Per ottenere informazioni su questi adapter, utilizzare la funzione [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .

La funzione [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) consente di recuperare gli indirizzi IP associati a un particolare adapter. Questa funzione supporta l'indirizzamento sia IPv4 che IPv6.

-   Per esempi di codice che coinvolgono [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , vedere [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

 

 



