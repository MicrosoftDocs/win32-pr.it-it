---
title: Cosa si può sapere e quando è possibile conoscerlo
description: Le applicazioni che sono sensibili agli stati indotti dalla latenza devono riconoscere gli Stati del problema ed eseguire l'azione appropriata.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297715"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="85fa4-103">Cosa si può sapere e quando è possibile conoscerlo?</span><span class="sxs-lookup"><span data-stu-id="85fa4-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="85fa4-104">Le applicazioni che sono sensibili agli stati indotti dalla latenza devono riconoscere gli Stati del problema ed eseguire l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="85fa4-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="85fa4-105">Ci sono due stati di problema: sfasamento della versione e aggiornamento parziale.</span><span class="sxs-lookup"><span data-stu-id="85fa4-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="85fa4-106">La distorsione della versione non è rilevabile esaminando il servizio directory (ricordare l'assioma del calcolo distribuito indicato nel [perché Active Directory Domain Services usare questo modello di replica](why-active-directory-domain-services-uses-this-replication-model.md)).</span><span class="sxs-lookup"><span data-stu-id="85fa4-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="85fa4-107">L'aggiornamento parziale può essere rilevato aggiungendo metadati agli oggetti che compongono il set correlato.</span><span class="sxs-lookup"><span data-stu-id="85fa4-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="85fa4-108">I suggerimenti per tali metadati vengono visualizzati nelle sezioni successive di questo documento.</span><span class="sxs-lookup"><span data-stu-id="85fa4-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="85fa4-109">È possibile adottare strategie di prevenzione per ridurre la possibilità di sfasamento della versione e di aggiornamento parziale.</span><span class="sxs-lookup"><span data-stu-id="85fa4-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="85fa4-110">Queste strategie vengono inoltre illustrate nelle sezioni successive di questo documento.</span><span class="sxs-lookup"><span data-stu-id="85fa4-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




