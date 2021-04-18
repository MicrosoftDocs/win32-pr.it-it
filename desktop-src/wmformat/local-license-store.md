---
title: Archivio licenze locale
description: Archivio licenze locale
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), licenze file protette
- DRM (Digital Rights Management), licenze file protette
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396843"
---
# <a name="local-license-store"></a><span data-ttu-id="87794-111">Archivio licenze locale</span><span class="sxs-lookup"><span data-stu-id="87794-111">Local License Store</span></span>

<span data-ttu-id="87794-112">Quando una licenza DRM viene recapitata al computer client, viene inserita nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="87794-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="87794-113">Si tratta di un file protetto sul disco rigido che contiene tutte le licenze rilasciate all'utente insieme ad altre informazioni di DRM.</span><span class="sxs-lookup"><span data-stu-id="87794-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="87794-114">È possibile modificare i dati nell'archivio licenze locale in pochi modi, usando le API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="87794-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="87794-115">Oltre all'archivio licenze locale, alcuni oggetti si avvaleno di un archivio licenze temporaneo.</span><span class="sxs-lookup"><span data-stu-id="87794-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="87794-116">Una licenza in un archivio temporaneo esiste solo per un breve periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="87794-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="87794-117">Tuttavia, alcune licenze che iniziano in un archivio temporaneo possono essere salvate nell'archivio licenze locale normale.</span><span class="sxs-lookup"><span data-stu-id="87794-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87794-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87794-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87794-119">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="87794-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




