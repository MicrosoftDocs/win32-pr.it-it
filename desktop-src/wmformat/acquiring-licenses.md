---
title: Acquisizione di licenze
description: Acquisizione di licenze
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, acquisizione di licenze
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), acquisizione di licenze
- DRM (Digital Rights Management), acquisizione di licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, acquisizione di licenze
- API estese client, acquisizione di licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395362"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="992bc-122">Acquisizione di licenze</span><span class="sxs-lookup"><span data-stu-id="992bc-122">Acquiring Licenses</span></span>

<span data-ttu-id="992bc-123">Uno scenario comune per l'acquisizione di licenze è quando un utente dispone di un file Windows Media protetto e tenta di accedere al contenuto per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="992bc-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="992bc-124">Poiché le API estese del client Windows Media DRM sono separate dalle routine di gestione dei file ASF, lo scenario di acquisizione della licenza di base, sebbene supportato, richiede più chiamate API rispetto all'uso di Windows Media Format SDK e di Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="992bc-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="992bc-125">Questa sezione descrive come usare le API estese del client Windows Media DRM per acquisire le licenze archiviate nell'archivio licenze locale in un computer client.</span><span class="sxs-lookup"><span data-stu-id="992bc-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="992bc-126">Contiene gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="992bc-126">It contains the following topics.</span></span>



| <span data-ttu-id="992bc-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="992bc-127">Topic</span></span>                                                                | <span data-ttu-id="992bc-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="992bc-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="992bc-129">Acquisizione di una licenza invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="992bc-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="992bc-130">Viene descritto come acquisire licenze senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="992bc-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="992bc-131">Acquisizione di licenza non invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="992bc-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="992bc-132">Viene descritto come acquisire licenze quando è richiesto l'intervento dell'utente, ad esempio il pagamento del contenuto.</span><span class="sxs-lookup"><span data-stu-id="992bc-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="992bc-133">Pre-distribuzione della licenza</span><span class="sxs-lookup"><span data-stu-id="992bc-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="992bc-134">Viene descritto come eseguire il pull delle licenze da un server licenze a un computer client.</span><span class="sxs-lookup"><span data-stu-id="992bc-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="992bc-135">Creazione di licenze localmente</span><span class="sxs-lookup"><span data-stu-id="992bc-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="992bc-136">Viene descritto come creare licenze personalizzate senza scaricarle da un server licenze e come archiviarle nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="992bc-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="992bc-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="992bc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="992bc-138">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="992bc-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




