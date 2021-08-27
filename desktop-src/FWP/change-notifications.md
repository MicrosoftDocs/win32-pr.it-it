---
title: Notifiche di modifica
description: Le Base Filtering Engine (BFE) seguono il modello di pubblicazione/sottoscrizione.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0038dc851cb15414dbc0180f205104725bf069b599632a93ae6e257fe7a1f84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078501"
---
# <a name="change-notifications"></a>Notifiche di modifica

Le notifiche di modifica Base Filtering Engine (BFE) seguono il modello di pubblicazione/sottoscrizione: per ricevere una delle notifiche di modifica pubblicate, un'applicazione deve sottoscriverla.

Le notifiche di modifica BFE pubblicate sono Add and Remove per [**callout,**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0) [**filters,**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0) [**providers,**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0) [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)e [**sub-layers.**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)

Per sottoscrivere una delle notifiche precedenti, un'applicazione chiama la funzione di gestione [**\* SubscribeChanges0 di Fwpm**](fwp-mgmt-functions.md) corrispondente, ad esempio [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0). La funzione di callback passata come argomento a **Fwpm \* SubscribeChanges0** viene richiamata da BFE quando si verifica la modifica a cui ha eseguito la sottoscrizione.

Per annullare la sottoscrizione a una delle notifiche precedenti, un'applicazione chiama la funzione di gestione **Fwpm \* UnsubscribeChanges0** corrispondente, ad esempio [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0).

Per visualizzare le sottoscrizioni correnti per una delle notifiche precedenti, un'applicazione chiama la funzione di gestione [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) corrispondente , ad esempio [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0).

Le notifiche di modifica offerte dal BFE sono:

-   Asincrona: la chiamata di funzione che ha attivato una notifica può restituire prima che la notifica sia stata inviata a tutti i sottoscrittori.
-   Inaffidabile: non viene garantita la corretta consegna delle notifiche.

I Sottoscrittori non ricevono notifiche per le modifiche apportate con l'handle di sessione usato per sottoscrivere. In genere, i sottoscrittori devono essere informati solo delle modifiche apportate da altri utenti. sanno già quali modifiche sono state apportate da sole.

 

 




