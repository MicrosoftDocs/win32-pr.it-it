---
title: Riferimento all'API di supporto per il routing della connessione su richiesta
description: Negli argomenti seguenti vengono fornite informazioni dettagliate sull'helper di routing della connessione su richiesta.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116921"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>Riferimento all'API di supporto per il routing della connessione su richiesta

Negli argomenti seguenti vengono fornite informazioni dettagliate sull'helper di routing della connessione su richiesta.



| Riferimento                                                                          | Descrizione                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Cercare una destinazione nella cache delle richieste di route e, se viene trovata una corrispondenza, restituisce l'ID di interfaccia corrispondente.<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Registrarsi per ricevere una notifica quando viene modificata la cache delle richieste di route.<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Annulla la registrazione per le notifiche e pulisci le risorse.<br/>                                                                                                             |
| [**\_contesto dell'interfaccia net \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | Contesto dell'interfaccia che fa parte della struttura [**della \_ \_ \_ tabella del contesto NET Interface**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .<br/>                                       |
| [**\_tabella del \_ contesto NET Interface \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | Tabella delle strutture [**di \_ \_ contesto dell'interfaccia .NET**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .<br/>                                                                                |
| [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Questa funzione recupera una tabella del contesto dell'interfaccia per il nome host e il filtro del profilo di connessione specificati.<br/>                                                         |
| [**FreeInterfaceContextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Questa funzione libera la tabella del contesto dell'interfaccia recuperata tramite la funzione [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .<br/> |



 

 

 





