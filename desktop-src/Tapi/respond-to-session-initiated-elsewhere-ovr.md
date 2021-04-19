---
description: Quando arriva una nuova sessione di comunicazione, le applicazioni TAPI che hanno registrato un interesse per l'indirizzo e il tipo di supporto riceveranno una notifica degli eventi.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Rispondere a una sessione avviata altrove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319868"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="ced5b-103">Rispondere a una sessione avviata altrove</span><span class="sxs-lookup"><span data-stu-id="ced5b-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="ced5b-104">Quando arriva una nuova sessione di comunicazione, le applicazioni TAPI che hanno registrato un interesse per l' [Indirizzo](address-ovr.md) e il [tipo di supporto](media-type-ovr.md) riceveranno una [notifica degli eventi](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ced5b-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="ced5b-105">Alla sessione verranno offerti [privilegi](privilege-ovr.md) di proprietà a una sola applicazione.</span><span class="sxs-lookup"><span data-stu-id="ced5b-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="ced5b-106">Questa applicazione non può rifiutare la sessione.</span><span class="sxs-lookup"><span data-stu-id="ced5b-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="ced5b-107">Lo stato di chiamata iniziale di una sessione in ingresso è offering.</span><span class="sxs-lookup"><span data-stu-id="ced5b-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="ced5b-108">Mentre la chiamata è nello stato dell'offerta, un'applicazione può ottenere informazioni, ad esempio la modalità di porta e il motivo della chiamata, se i provider di servizi hanno fornito queste informazioni e sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="ced5b-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="ced5b-109">Alcune informazioni sulle chiamate potrebbero non essere immediatamente disponibili, ad esempio l'ID chiamante.</span><span class="sxs-lookup"><span data-stu-id="ced5b-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="ced5b-110">Sono disponibili sei risposte di base a una sessione offerta [: risposta](answer-ovr.md), [accettazione](accept-ovr.md), [consegna, rilascio](drop-ovr.md), [invio](forward-ovr.md)e [Reindirizzamento](redirect-ovr.md). [](handoffs-ovr.md)</span><span class="sxs-lookup"><span data-stu-id="ced5b-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="ced5b-111">A seconda del provider di servizi, il set completo di queste operazioni potrebbe non essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="ced5b-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



