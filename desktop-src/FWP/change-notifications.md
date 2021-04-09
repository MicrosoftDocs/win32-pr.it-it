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
# <a name="change-notifications"></a><span data-ttu-id="59914-103">Notifiche delle modifiche</span><span class="sxs-lookup"><span data-stu-id="59914-103">Change Notifications</span></span>

<span data-ttu-id="59914-104">Le notifiche di modifica BFE (Base Filtering Engine) seguono il modello di pubblicazione/sottoscrizione: per ricevere una delle notifiche di modifica pubblicate, un'applicazione deve sottoscriverla.</span><span class="sxs-lookup"><span data-stu-id="59914-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="59914-105">Le notifiche di modifica BFE pubblicate sono Aggiungi e Rimuovi per [**callout**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filtri**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**provider**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**contesti di provider**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)e [**sottolivelli**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span><span class="sxs-lookup"><span data-stu-id="59914-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="59914-106">Per sottoscrivere una delle notifiche precedenti, un'applicazione chiama la funzione di [**gestione \* SubscribeChanges0 Fwpm**](fwp-mgmt-functions.md) corrispondente (ad esempio, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="59914-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="59914-107">La funzione di callback passata come argomento a **Fwpm \* SubscribeChanges0** viene richiamata da BFE quando si verifica la modifica della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="59914-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="59914-108">Per annullare la sottoscrizione di una delle notifiche precedenti, un'applicazione chiama la funzione di gestione **\* UnsubscribeChanges0 Fwpm** corrispondente (ad esempio, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="59914-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="59914-109">Per visualizzare le sottoscrizioni correnti per una delle notifiche precedenti, un'applicazione chiama la funzione di gestione [**\* SubscriptionsGet0 Fwpm**](fwp-mgmt-functions.md) corrispondente (ad esempio [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span><span class="sxs-lookup"><span data-stu-id="59914-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="59914-110">Le notifiche di modifica offerte da BFE sono:</span><span class="sxs-lookup"><span data-stu-id="59914-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="59914-111">Asincrono: la chiamata di funzione che ha attivato una notifica può restituire prima che la notifica sia stata inviata a tutti i sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="59914-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="59914-112">Non affidabile: non viene garantita alcuna garanzia che le notifiche vengano recapitate correttamente.</span><span class="sxs-lookup"><span data-stu-id="59914-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="59914-113">I Sottoscrittori non ricevono notifiche per le modifiche apportate con l'handle di sessione usato per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="59914-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="59914-114">In genere, i Sottoscrittori devono essere informati solo delle modifiche apportate da altri utenti; sanno già quali modifiche sono state apportate da soli.</span><span class="sxs-lookup"><span data-stu-id="59914-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 




