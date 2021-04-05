---
title: Riquadri attività servizio
description: Riquadri attività servizio
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player Online Stores, riquadri attività servizio
- archivi online, riquadri attività del servizio
- digitare 2 archivi online, riquadri attività servizio
- Windows Media Player Online Stores, riquadri attività
- archivi online, riquadri attività
- digitare 2 archivi online, riquadri attività
- Media Player di Windows, riquadri attività servizio
- Media Player di Windows, riquadri attività
- riquadri attività servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044860"
---
# <a name="service-task-panes"></a><span data-ttu-id="051bf-112">Riquadri attività servizio</span><span class="sxs-lookup"><span data-stu-id="051bf-112">Service Task Panes</span></span>

<span data-ttu-id="051bf-113">In Windows Media Player 10, i provider di archivio online possono configurare Windows Media Player per visualizzare fino a tre riquadri attività, detti riquadri attività del servizio.</span><span class="sxs-lookup"><span data-stu-id="051bf-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="051bf-114">Ogni riquadro attività del servizio è rappresentato da un pulsante personalizzabile visualizzato da Windows Media Player sul lato destro della barra delle applicazioni delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="051bf-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="051bf-115">Ogni riquadro attività del servizio ospita una pagina Web che rappresenta l'interfaccia utente per una particolare funzionalità di negozio online. L'aspetto dei riquadri attività del servizio è definito dal documento XML ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="051bf-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="051bf-116">In questo documento i riquadri attività del servizio sono rappresentati da tre elementi: **ServiceTask1**, **ServiceTask2** e **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="051bf-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="051bf-117">Questi riquadri attività del servizio sono progettati per fornire quanto segue:</span><span class="sxs-lookup"><span data-stu-id="051bf-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="051bf-118">Un servizio musicale.</span><span class="sxs-lookup"><span data-stu-id="051bf-118">A music service.</span></span>
-   <span data-ttu-id="051bf-119">Un servizio video.</span><span class="sxs-lookup"><span data-stu-id="051bf-119">A video service.</span></span>
-   <span data-ttu-id="051bf-120">Un servizio radio.</span><span class="sxs-lookup"><span data-stu-id="051bf-120">A radio service.</span></span>

<span data-ttu-id="051bf-121">È possibile posizionare queste funzionalità in Windows Media Player in qualsiasi ordine, ma è necessario che **ServiceTask1** sia il riquadro attività principale per l'attivazione delle attività commerciali.</span><span class="sxs-lookup"><span data-stu-id="051bf-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="051bf-122">La pagina Web ospitata in ogni riquadro attività del servizio può accedere all'oggetto **esterno** .</span><span class="sxs-lookup"><span data-stu-id="051bf-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="051bf-123">Questo oggetto fornisce metodi, proprietà e un evento che forniscono funzionalità speciali per le pagine Web in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="051bf-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="051bf-124">Ad esempio, è possibile usare l'evento e le proprietà da **External** per fare in modo che l'aspetto della pagina Web corrisponda alla combinazione di colori scelta dall'utente per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="051bf-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="051bf-125">In Windows Media Player 11 non sono presenti riquadri attività del servizio.</span><span class="sxs-lookup"><span data-stu-id="051bf-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="051bf-126">È invece disponibile una singola scheda **Store online** che ospita la pagina Web principale per lo Store online attivo.</span><span class="sxs-lookup"><span data-stu-id="051bf-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="051bf-127">Nel documento ServiceInfo la scheda **Store online** è rappresentata dall'elemento **ServiceTask1** . gli elementi **ServiceTask2** e **ServiceTask3** vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="051bf-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="051bf-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="051bf-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="051bf-129">**Informazioni sui negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="051bf-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="051bf-130">**Oggetto esterno per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="051bf-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="051bf-131">**Documento ServiceInfo per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="051bf-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




