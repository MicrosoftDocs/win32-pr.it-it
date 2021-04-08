---
title: Blocco evento
description: Blocco evento
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856045"
---
# <a name="event-freezing"></a><span data-ttu-id="35b96-103">Blocco evento</span><span class="sxs-lookup"><span data-stu-id="35b96-103">Event Freezing</span></span>

<span data-ttu-id="35b96-104">Un contenitore può notificare a un controllo che non è pronto a rispondere agli eventi chiamando [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true**.</span><span class="sxs-lookup"><span data-stu-id="35b96-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="35b96-105">Può sbloccare gli eventi chiamando **FreezeEvents** con **false**.</span><span class="sxs-lookup"><span data-stu-id="35b96-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="35b96-106">Quando un contenitore blocca gli eventi, è in corso il blocco dell'elaborazione degli eventi, non la ricezione di eventi; ovvero, un contenitore può comunque ricevere eventi mentre gli eventi vengono bloccati.</span><span class="sxs-lookup"><span data-stu-id="35b96-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="35b96-107">Se un contenitore riceve una notifica degli eventi mentre i relativi eventi sono bloccati, il contenitore deve ignorare l'evento.</span><span class="sxs-lookup"><span data-stu-id="35b96-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="35b96-108">Non sono necessarie altre azioni.</span><span class="sxs-lookup"><span data-stu-id="35b96-108">No other action is appropriate.</span></span>

<span data-ttu-id="35b96-109">Un controllo deve prendere nota della chiamata di un contenitore a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true** se è importante per il controllo che un evento non viene perso.</span><span class="sxs-lookup"><span data-stu-id="35b96-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="35b96-110">Mentre l'elaborazione degli eventi di un contenitore è bloccata, un controllo deve implementare una delle tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="35b96-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="35b96-111">Attivare gli eventi con la massima consapevolezza che il contenitore non eseguirà alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="35b96-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="35b96-112">Rimuovere tutti gli eventi che il controllo avrebbe generato.</span><span class="sxs-lookup"><span data-stu-id="35b96-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="35b96-113">Accodare tutti gli eventi in sospeso e attivarli dopo che il contenitore ha chiamato [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.</span><span class="sxs-lookup"><span data-stu-id="35b96-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="35b96-114">Accodare solo gli eventi rilevanti o importanti e attivarli dopo che il contenitore ha chiamato [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.</span><span class="sxs-lookup"><span data-stu-id="35b96-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="35b96-115">Ogni tecnica è accettabile e appropriata in circostanze diverse.</span><span class="sxs-lookup"><span data-stu-id="35b96-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="35b96-116">Lo sviluppatore del controllo è responsabile della determinazione e dell'implementazione della tecnica appropriata per la funzionalità del controllo.</span><span class="sxs-lookup"><span data-stu-id="35b96-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 




