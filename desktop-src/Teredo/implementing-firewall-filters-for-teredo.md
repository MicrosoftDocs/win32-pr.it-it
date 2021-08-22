---
title: Implementazione di filtri firewall per Teredo
description: Windows consente alle applicazioni di impostare un'opzione socket che consente alle applicazioni di indicare una finalità esplicita di ricevere il traffico Teredo inviato al firewall host tramite Windows Filtering Platform.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe854b210e6b07f0777a492d5c952f502e2f7c2b6c1c4b40497bad3a9e8248a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001810"
---
# <a name="implementing-firewall-filters-for-teredo"></a>Implementazione di filtri firewall per Teredo

Windows consente alle applicazioni di impostare un'opzione socket che consente alle applicazioni di indicare una finalità esplicita di ricevere il traffico Teredo inviato al firewall host tramite Windows Filtering Platform. In Windows, viene usata un'opzione socket per l'impostazione di un livello di protezione per consentire a un'applicazione di definire il tipo di traffico che è disposto a ricevere. In particolare, negli scenari che coinvolgono Teredo traffico, viene specificata [l'opzione socket IPV6 \_ PROTECTION \_ LEVEL.](/windows/desktop/WinSock/ipv6-protection-level) È consigliabile che le implementazioni del firewall host mantengano i filtri seguenti per consentire Teredo modo selettivo il traffico per un'applicazione, bloccando il traffico per impostazione predefinita per qualsiasi applicazione senza esenzione.

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Filtro di blocco predefinito per il traffico edge attraversato

Un firewall host deve sempre mantenere un filtro di blocco predefinito all'interno del livello di filtro ALE \_ AUTH RECV ACCEPT V6 per il traffico corrispondente alle condizioni di Tunnel e Tunnel \_ \_ Type \_ **Teredo** specificati.  In caso di implementazione, questo filtro indica la presenza di un firewall host in grado di riconoscere l'attraversamento perimetrale nel sistema. Questo filtro viene visualizzato come contratto API tra il firewall host e Windows. Per impostazione predefinita, questo filtro blocca il traffico edge attraversato verso qualsiasi applicazione.

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> Le classi "Delivery", "Arrival" e "Next Hop" delle condizioni dell'interfaccia vengono usate per controllare un modello di host debole e l'inoltro di pacchetti tra le interfacce. Nell'esempio precedente viene utilizzata la classe "Delivery". Vedere [Condizioni di filtro disponibili a ogni livello di](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) filtro nella documentazione di WFP SDK, in quanto la progettazione della sicurezza deve prendere in considerazione ogni caso.

 

## <a name="allow-filter-for-exempt-applications"></a>Consenti filtro per le applicazioni esentate

Se un'applicazione è esente dalla ricezione di traffico Teredo un socket di ascolto, è necessario che nel livello di filtro \_ \_ AUTH RCV ACCEPT V6 di ALE sia implementato un filtro di autorizzazione nel \_ \_ firewall host. È importante notare che, a seconda della configurazione dell'esenzione da parte dell'utente o dell'applicazione, il firewall host può includere un'opzione socket.

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a>Filtro callout inattivo

Il Teredo in Windows implementa un modello inattivo. In qualsiasi momento, se nessuna applicazione è in ascolto su un socket UDP o TCP con attraversamento perimetrale abilitato, il servizio passa a uno stato inattivo. Per il funzionamento del meccanismo di inattivazione, il firewall host deve mantenere un filtro callout per ogni applicazione esente specificata nel livello di filtro ALE AUTH LISTEN V6 per TCP e nel livello di filtro \_ \_ \_ ALE \_ RESOURCE ASSIGNMENT \_ V6 per le applicazioni basate su \_ UDP. L'esempio seguente illustra un callout inattivo per **un'applicazione TCP.**

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 