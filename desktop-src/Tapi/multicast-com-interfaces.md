---
description: Le interfacce COM multicast consentono l'accesso alla funzionalità reti per l'allocazione, il rinnovo e il rilascio di lease sugli indirizzi multicast.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Interfacce COM multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749530"
---
# <a name="multicast-com-interfaces"></a>Interfacce COM multicast

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Le interfacce COM multicast consentono l'accesso alla funzionalità della rete per l'allocazione, il rinnovo e il rilascio di lease sugli indirizzi multicast. Incapsulano un set di definizioni di strutture di dati e funzioni. Le interfacce COM liberano il programmatore dalla difficoltà di comprendere e modificare queste strutture di dati. Inoltre, poiché TAPI 3 è basato su COM, queste interfacce rendono accessibile l'allocazione di indirizzi multicast in modo coerente con le altre funzionalità offerte da TAPI 3. Le applicazioni scritte con Visual Basic, Java o linguaggi di scripting che in genere non possono accedere direttamente all'API di Windows sono in grado di usare queste interfacce.

L'allocazione di indirizzi multicast è attualmente l'oggetto di un gruppo di lavoro IETF. Per accedere alle informazioni correnti, eseguire una query su "MDHCP" o "MADCAP" e "Internet Draft" utilizzando un motore di ricerca Internet. Oltre a MADCAP, l'architettura proposta include un protocollo per il coordinamento da server a server all'interno di un dominio o come, oltre a un protocollo per il coordinamento tra domini. Mentre questa architettura è in continua evoluzione, il client non deve preoccuparsi di se stesso con i dettagli di questo schema.

Questo componente supporta attualmente solo indirizzi IP versione 4.

> [!Note]  
> Il protocollo usato per queste interfacce è attualmente denominato MADCAP. Nelle versioni precedenti era noto come MDHCP.

 

L'oggetto multicast viene creato chiamando **CoCreateInstance** sull'interfaccia [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) . L'interfaccia **IMcastAddressAllocation** espone il metodo [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) , che consente a un'applicazione di ottenere un elenco di tutti gli ambiti multicast disponibili.

Una volta ottenuto un ambito di lavoro, viene utilizzato il metodo [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) per richiedere un indirizzo multicast dal server. Se la richiesta ha esito positivo, viene restituito un puntatore [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) . Il metodo [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) esposto da questa interfaccia può quindi essere utilizzato per ottenere gli indirizzi.

Ogni oggetto multimediale associato alla conferenza espone un'interfaccia [**ITConnection**](itconnection.md) . Il metodo [**ITConnection:: SetAddressInfo**](itconnection-setaddressinfo.md) consente l'assegnazione degli indirizzi multicast ottenuti al supporto della conferenza. È necessario impostare l'indirizzo per ogni interfaccia **ITConnection** di ogni oggetto multimediale associato alla conferenza.

 

 



