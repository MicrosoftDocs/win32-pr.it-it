---
description: Le interfacce COM multicast consentono l'accesso alla struttura di reti per l'allocazione, il rinnovo e il rilascio di lease su indirizzi multicast.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Interfacce COM multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c87c231f18904e3b0287095f511cf3c82bfd263e23a9e69dd50c02eb491616d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575541"
---
# <a name="multicast-com-interfaces"></a>Interfacce COM multicast

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Le interfacce COM multicast consentono l'accesso alla struttura della rete per l'allocazione, il rinnovo e il rilascio di lease su indirizzi multicast. Incapsulano un set di definizioni di funzioni e strutture di dati. Le interfacce COM liberano il programmatore dall'onere di comprendere e modificare queste strutture di dati. Inoltre, poiché TAPI 3 è basato su COM, queste interfacce rendono accessibile l'allocazione di indirizzi multicast in modo coerente con le altre funzionalità fornite da TAPI 3. Le applicazioni scritte Visual Basic, Java o linguaggi di scripting che normalmente non possono accedere direttamente all'API Windows possono usare queste interfacce.

L'allocazione di indirizzi multicast è attualmente oggetto di un gruppo di lavoro IETF. Per accedere alle informazioni correnti, eseguire una query su "MDHCP" o "MADCAP" e "bozza Internet" usando qualsiasi motore di ricerca Internet. Oltre a MADCAP, l'architettura proposta include un protocollo per il coordinamento da server a server all'interno di un dominio o as, nonché un protocollo per il coordinamento tra domini. Anche se questa architettura è attualmente in evoluzione, il client non deve riguardare se stesso con i dettagli di questo schema.

Questo componente attualmente supporta solo indirizzi IP versione 4.

> [!Note]  
> Il protocollo usato per queste interfacce è attualmente denominato MADCAP. Nelle versioni precedenti era noto come MDHCP.

 

L'oggetto multicast viene creato chiamando **CoCreateInstance** [**sull'interfaccia IMcastAddressAllocation.**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) **L'interfaccia IMcastAddressAllocation** espone il [**metodo EnumerateScopes,**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) che consente a un'applicazione di ottenere un elenco di tutti gli ambiti multicast disponibili.

Dopo aver ottenuto un ambito funzionante, il [**metodo RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) viene usato per richiedere un indirizzo multicast dal server. Se la richiesta ha esito positivo, viene [**restituito un puntatore IMcastLeaseInfo.**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) Il [**metodo EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) esposto da questa interfaccia può quindi essere usato per ottenere gli indirizzi.

Ogni oggetto Media associato alla conferenza espone [**un'interfaccia ITConnection.**](itconnection.md) Il [**metodo ITConnection::SetAddressInfo**](itconnection-setaddressinfo.md) consente l'assegnazione degli indirizzi multicast ottenuti ai supporti della conferenza. L'indirizzo deve essere impostato per ogni **interfaccia ITConnection** di ogni oggetto Media associato alla conferenza.

 

 



