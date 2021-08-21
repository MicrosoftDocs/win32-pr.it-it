---
description: L'helper IP offre funzionalità per la gestione delle schede di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adattatori in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre una scheda è un'astrazione a livello di collegamento dati.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gestione delle schede di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e1fd02426b27e3c07d4634edbe0215efa1c5c25c7a9c3abde32e991f766daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078261"
---
# <a name="managing-network-adapters"></a>Gestione delle schede di rete

L'helper IP offre funzionalità per la gestione delle schede di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adattatori in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre una scheda è un'astrazione a livello di collegamento dati.

Usare le funzioni descritte nei paragrafi seguenti per recuperare informazioni sulle schede di rete nel computer locale.

La [**funzione GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) restituisce una matrice di [**strutture IP ADAPTER \_ \_ INFO,**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) una per ogni scheda nel computer locale. La [**funzione GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) restituisce informazioni aggiuntive su un adattatore specifico. La **funzione GetPerAdapterInfo** richiede al chiamante di specificare l'indice dell'adapter. Per ottenere l'indice dell'adapter dal nome dell'adapter, usare la [**funzione GetAdapterIndex.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex)

Alcune applicazioni usano adattatori che ricevono datagrammi, ma non possono trasmetterli. Per ottenere informazioni su questi adattatori, usare la [**funzione GetUniDirectionalAdapterInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

La [**funzione GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) consente di recuperare gli indirizzi IP associati a una scheda specifica. Questa funzione supporta l'indirizzamento sia IPv4 che IPv6.

-   Per esempi di codice relativi [**a GetAdaptersInfo,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) vedere [Gestione di schede di rete tramite GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

 

 



