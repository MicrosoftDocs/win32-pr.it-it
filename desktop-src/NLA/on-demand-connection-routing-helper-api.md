---
title: Informazioni di riferimento sull'API helper routing di connessione su richiesta
description: Gli argomenti seguenti forniscono informazioni dettagliate sull'helper di routing di connessione su richiesta.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e046c1add8703e6603d925d2c80b03aab8d7eae3a352825e56ec907f3adb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685581"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>Informazioni di riferimento sull'API helper routing di connessione su richiesta

Gli argomenti seguenti forniscono informazioni dettagliate sull'helper di routing di connessione su richiesta.



| Riferimento                                                                          | Descrizione                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Cercare una destinazione nella cache delle richieste di route e, se viene trovata una corrispondenza, restituisce l'ID interfaccia corrispondente.<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Registrarsi per ricevere una notifica quando viene modificata la cache delle richieste di route.<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Annullare la registrazione per le notifiche e pulire le risorse.<br/>                                                                                                             |
| [**CONTESTO \_ DELL'INTERFACCIA \_ DI RETE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | Contesto dell'interfaccia che fa parte della struttura [**NET \_ INTERFACE CONTEXT \_ \_ TABLE.**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)<br/>                                       |
| [**TABELLA \_ DEL CONTESTO \_ \_ DELL'INTERFACCIA DI RETE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | Tabella delle [**strutture NET INTERFACE \_ \_ CONTEXT.**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)<br/>                                                                                |
| [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Questa funzione recupera una tabella di contesto dell'interfaccia per il nome host e il filtro del profilo di connessione specificati.<br/>                                                         |
| [**FreeInterfaceContextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Questa funzione libera la tabella del contesto dell'interfaccia recuperata usando la [**funzione GetInterfaceContextTableForHostName.**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname)<br/> |



 

 

 





