---
title: Introduzione agli utenti di Windows Media Format SDK
description: Introduzione agli utenti di Windows Media Format SDK
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- API estese del client DRM, informazioni
- API estese client, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396074"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="cc0f4-116">Introduzione agli utenti di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="cc0f4-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="cc0f4-117">Gran parte delle funzionalità fornite dalle API estese del client Windows Media DRM è la stessa della funzionalità fornita dagli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="cc0f4-118">Windows Media Format SDK fornisce agli sviluppatori gli oggetti necessari per creare, accedere e modificare i file multimediali che usano la struttura di file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="cc0f4-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="cc0f4-119">Poiché Windows Media DRM è progettato per proteggere i file ASF, la funzionalità DRM sul lato client è stata inclusa in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="cc0f4-120">Le API estese del client Windows Media DRM sono state rilasciate insieme alla piattaforma multimediale digitale di prossima generazione Microsoft, il Microsoft Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="cc0f4-121">Media Foundation includerà la funzionalità ASF che si sovrappone ad alcune delle funzionalità di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="cc0f4-122">Poiché ora esistono due SDK Microsoft che modificano i file ASF, la funzionalità DRM sul lato client viene separata da Windows Media Format SDK nelle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="cc0f4-123">È possibile accedere a queste API dagli utenti di Windows Media Format SDK e di Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="cc0f4-124">Al momento, queste API sono incluse come parte del pacchetto di installazione di Windows Media Format SDK e sono documentate come parte di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="cc0f4-125">Tuttavia, le API estese del client Windows Media DRM sono implementate nella propria libreria e hanno un proprio file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="cc0f4-126">Dopo l'installazione di Windows Media Format SDK, queste API possono essere utilizzate una propria, senza includere intestazioni o librerie di Windows Media Format SDK nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="cc0f4-127">Se si sviluppano applicazioni che utilizzano Windows Media Format SDK, è necessario decidere se utilizzare la funzionalità DRM fornita dall'SDK oppure utilizzare le API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="cc0f4-128">Sebbene molte delle funzionalità di questi due SDK siano molto simili, le API estese del client Windows Media DRM offrono le seguenti funzionalità non disponibili per gli utenti delle routine DRM precedenti:</span><span class="sxs-lookup"><span data-stu-id="cc0f4-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="cc0f4-129">Possibilità di importare contenuti protetti da un sistema di Rights Management di terze parti.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="cc0f4-130">Possibilità di esportare contenuti protetti da DRM di Windows Media in un sistema di Rights Management di terze parti.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="cc0f4-131">Enumerazione diretta delle licenze nell'archivio licenze.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="cc0f4-132">Semplice esecuzione di query sui diritti aggregati in base all'ID chiave (non è necessario caricare il file multimediale).</span><span class="sxs-lookup"><span data-stu-id="cc0f4-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="cc0f4-133">Possibilità di rinnovare i componenti revocati usando l'interfaccia Media Foundation standard, **IMFContentEnabler**.</span><span class="sxs-lookup"><span data-stu-id="cc0f4-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc0f4-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc0f4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc0f4-135">**Informazioni sulle API estese del client Windows Media DRM**</span><span class="sxs-lookup"><span data-stu-id="cc0f4-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




