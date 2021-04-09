---
title: Notifiche delle modifiche
description: Le notifiche di modifica BFE (Base Filtering Engine) seguono il modello di pubblicazione/sottoscrizione.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103956209"
---
# <a name="change-notifications"></a>Notifiche delle modifiche

Le notifiche di modifica BFE (Base Filtering Engine) seguono il modello di pubblicazione/sottoscrizione: per ricevere una delle notifiche di modifica pubblicate, un'applicazione deve sottoscriverla.

Le notifiche di modifica BFE pubblicate sono Aggiungi e Rimuovi per [**callout**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filtri**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**provider**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**contesti di provider**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)e [**sottolivelli**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).

Per sottoscrivere una delle notifiche precedenti, un'applicazione chiama la funzione di [**gestione \* SubscribeChanges0 Fwpm**](fwp-mgmt-functions.md) corrispondente (ad esempio, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). La funzione di callback passata come argomento a **Fwpm \* SubscribeChanges0** viene richiamata da BFE quando si verifica la modifica della sottoscrizione.

Per annullare la sottoscrizione di una delle notifiche precedenti, un'applicazione chiama la funzione di gestione **\* UnsubscribeChanges0 Fwpm** corrispondente (ad esempio, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Per visualizzare le sottoscrizioni correnti per una delle notifiche precedenti, un'applicazione chiama la funzione di gestione [**\* SubscriptionsGet0 Fwpm**](fwp-mgmt-functions.md) corrispondente (ad esempio [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

Le notifiche di modifica offerte da BFE sono:

-   Asincrono: la chiamata di funzione che ha attivato una notifica può restituire prima che la notifica sia stata inviata a tutti i sottoscrittori.
-   Non affidabile: non viene garantita alcuna garanzia che le notifiche vengano recapitate correttamente.

I Sottoscrittori non ricevono notifiche per le modifiche apportate con l'handle di sessione usato per la sottoscrizione. In genere, i Sottoscrittori devono essere informati solo delle modifiche apportate da altri utenti; sanno già quali modifiche sono state apportate da soli.

 

 




