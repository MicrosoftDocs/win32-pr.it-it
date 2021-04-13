---
title: Chiavi di test e di produzione per un archivio online di tipo 1
description: Chiavi di test e di produzione per un archivio online di tipo 1
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Windows Media Player Online Store, chiavi di test
- archivi online, chiavi di test
- digitare 1 archivi online, chiavi di test
- Windows Media Player Online Store, chiavi di produzione
- archivi online, chiavi di produzione
- digitare 1 negozi online, chiavi di produzione
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- test chiavi
- chiavi di produzione
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e8ce8d049df78f186d336079f76eb00eb8bb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396651"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a><span data-ttu-id="c7329-115">Chiavi di test e di produzione per un archivio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="c7329-115">Test and Production Keys for a Type 1 Online Store</span></span>

<span data-ttu-id="c7329-116">Quando si inizia lo sviluppo dello Store online, Microsoft fornisce due chiavi numeriche: una chiave di test e una chiave di produzione.</span><span class="sxs-lookup"><span data-stu-id="c7329-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="c7329-117">Allo stesso tempo, è necessario fornire a Microsoft due URL: uno che punta al documento ServiceInfo di test e uno che fa riferimento al documento ServiceInfo di produzione.</span><span class="sxs-lookup"><span data-stu-id="c7329-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="c7329-118">Durante la fase di sviluppo e test, il negozio online è visibile in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c7329-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="c7329-119">Se la chiave di test si trova nel registro di sistema, Windows Media Player Recupera il documento ServiceInfo di test, che fa riferimento al plug-in, alle pagine Web e alle immagini che appartengono all'archivio di test.</span><span class="sxs-lookup"><span data-stu-id="c7329-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="c7329-120">Se la chiave di produzione si trova nel registro di sistema, Windows Media Player Recupera il documento ServiceInfo di produzione, che fa riferimento al plug-in, alle pagine Web e alle immagini che appartengono all'archivio di produzione.</span><span class="sxs-lookup"><span data-stu-id="c7329-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="c7329-121">È possibile usare gli archivi di test e di produzione in qualsiasi modo utile.</span><span class="sxs-lookup"><span data-stu-id="c7329-121">You can use your test and production stores in any way that you find useful.</span></span> <span data-ttu-id="c7329-122">In genere, tuttavia, la distinzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c7329-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="c7329-123">L'archivio di test è il punto in cui vengono apportate modifiche quotidiane al plug-in, alle pagine Web, alle immagini e ad altri componenti del servizio.</span><span class="sxs-lookup"><span data-stu-id="c7329-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="c7329-124">Lo Store di produzione è il luogo in cui si mantiene una versione stabile del servizio, che include il plug-in, le pagine Web, le immagini e altri componenti.</span><span class="sxs-lookup"><span data-stu-id="c7329-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="c7329-125">Prima di poter pubblicare l'archivio online in Windows Media Player, Microsoft deve verificare che il servizio venga eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c7329-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="c7329-126">Durante la fase di convalida, Microsoft usa la chiave di produzione.</span><span class="sxs-lookup"><span data-stu-id="c7329-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="c7329-127">Microsoft non utilizza la chiave di test durante la fase di convalida.</span><span class="sxs-lookup"><span data-stu-id="c7329-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="c7329-128">Quando l'archivio online di produzione completa correttamente il processo di convalida, Microsoft pubblica l'archivio, il che significa che l'archivio di produzione viene visualizzato in Windows Media Player per tutti gli utenti, non solo quelli che hanno la chiave di produzione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7329-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="c7329-129">Dopo la pubblicazione del negozio, le chiavi di test e di produzione non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="c7329-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="c7329-130">Gli utenti potrebbero essere in grado di indovinare la chiave di test o di produzione per il negozio online e visualizzare l'archivio mentre è in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="c7329-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="c7329-131">È necessario prestare attenzione a esporre le funzionalità che si desidera tenere segrete fino alla versione pubblica.</span><span class="sxs-lookup"><span data-stu-id="c7329-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="c7329-132">Per informazioni dettagliate sulla posizione in cui inserire le chiavi di produzione e di test nel registro di sistema dell'utente, vedere [chiavi e voci del registro di sistema per un archivio di tipo 1 online](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="c7329-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7329-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7329-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7329-134">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="c7329-134">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




