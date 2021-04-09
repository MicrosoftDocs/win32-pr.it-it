---
title: Ricerca di un driver specifico
description: Ricerca di un driver specifico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Gestione compressione audio (ACM), ricerca dei driver
- ACM (Gestione compressione audio), ricerca di driver
- Esempi di ACM, ricerca di driver
- ricerca di driver
- acmDriverEnum (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856754"
---
# <a name="finding-a-specific-driver"></a><span data-ttu-id="4dc30-108">Ricerca di un driver specifico</span><span class="sxs-lookup"><span data-stu-id="4dc30-108">Finding a Specific Driver</span></span>

<span data-ttu-id="4dc30-109">Potrebbe essere necessario che l'applicazione invii un messaggio direttamente a un driver specifico o per identificare determinati driver dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="4dc30-109">You might want your application to send a message directly to a specific driver or to identify certain drivers from the list.</span></span> <span data-ttu-id="4dc30-110">È ad esempio possibile che l'applicazione identifichi i driver che supportano i filtri, quindi esegue una query su ogni driver per determinare quali tag di filtro sono supportati.</span><span class="sxs-lookup"><span data-stu-id="4dc30-110">For example, you might want your application to identify those drivers that support filters and then query each driver to determine which filter tags it supports.</span></span> <span data-ttu-id="4dc30-111">È possibile utilizzare la funzione [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) per ottenere un handle per il driver o i driver desiderati. Questo handle può quindi essere utilizzato per comunicare con tale driver.</span><span class="sxs-lookup"><span data-stu-id="4dc30-111">You can use the [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) function to obtain a handle to the desired driver or drivers; this handle can then be used to communicate with that driver.</span></span>

<span data-ttu-id="4dc30-112">Si noti che quando un'applicazione installa un driver locale per uso personale, la funzione [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) restituisce un handle del driver, che può essere usato per comunicare con il driver.</span><span class="sxs-lookup"><span data-stu-id="4dc30-112">Note that when an application installs a local driver for its own use, the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function returns a driver handle, which can be used to communicate with the driver.</span></span> <span data-ttu-id="4dc30-113">In questo caso, non è necessario usare **acmDriverEnum** .</span><span class="sxs-lookup"><span data-stu-id="4dc30-113">It is not necessary to use **acmDriverEnum** in this case.</span></span>

 

 




