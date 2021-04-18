---
title: Integrazione della funzionalità di visualizzazione del centro informazioni
description: Integrazione della funzionalità di visualizzazione del centro informazioni
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player Online Stores, integrazione della vista di Info Center
- negozi online, integrazione della vista di Info Center
- digitare 1 negozi online, integrazione della visualizzazione di Info Center
- digitare 2 archivi online, integrando la visualizzazione di Info Center
- Windows Media Player Online Stores, visualizzazione centro informazioni
- negozi online, visualizzazione centro informazioni
- digitare 1 negozi online, visualizzazione centro informazioni
- digitare 2 archivi online, visualizzazione centro informazioni
- integrazione di visualizzazione centro informazioni
- Visualizzazione centro informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298847"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="7f252-113">Integrazione della funzionalità di visualizzazione del centro informazioni</span><span class="sxs-lookup"><span data-stu-id="7f252-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="7f252-114">Windows Media Player consente agli utenti di aprire e chiudere la funzionalità Visualizzazione del centro informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f252-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="7f252-115">La visualizzazione centro informazioni è la funzionalità in cui gli utenti si aspettano di trovare informazioni dettagliate e estese su contenuto multimediale digitale specifico.</span><span class="sxs-lookup"><span data-stu-id="7f252-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="7f252-116">Quando l'utente sceglie di aprire la visualizzazione del centro informazioni, Windows Media Player chiama sull'archivio musica corrente per visualizzare la pagina Web visualizzazione del centro informazioni specificata dall'attributo **URL** **dell'elemento del** centro informazioni del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="7f252-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="7f252-117">Per recuperare informazioni sul contenuto multimediale digitale attualmente in riproduzione, è necessario incorporare un'istanza del controllo Media Player Windows nella pagina Web e utilizzare il modello a oggetti del lettore.</span><span class="sxs-lookup"><span data-stu-id="7f252-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="7f252-118">Per recuperare il titolo, ad esempio, è possibile usare il codice JScript seguente:</span><span class="sxs-lookup"><span data-stu-id="7f252-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="7f252-119">Linee guida per la visualizzazione centro informazioni</span><span class="sxs-lookup"><span data-stu-id="7f252-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="7f252-120">Quando si crea la pagina Web **visualizzazione centro informazioni** , attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f252-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="7f252-121">La pagina deve identificare chiaramente l'archivio online che fornisce le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f252-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="7f252-122">A tale scopo, è possibile visualizzare in primo piano il logo, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="7f252-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="7f252-123">La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="7f252-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="7f252-124">Evitare l'esplorazione delle pagine all'interno della funzionalità di visualizzazione del centro informazioni quando possibile.</span><span class="sxs-lookup"><span data-stu-id="7f252-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="7f252-125">Per la maggior parte delle attività, è necessario passare all'archivio online.</span><span class="sxs-lookup"><span data-stu-id="7f252-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="7f252-126">È preferibile fornire informazioni preziose senza richiedere all'utente di installare programmi o accedere al proprio negozio online.</span><span class="sxs-lookup"><span data-stu-id="7f252-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f252-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f252-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f252-128">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="7f252-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="7f252-129">**Elemento centro informazioni**</span><span class="sxs-lookup"><span data-stu-id="7f252-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="7f252-130">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="7f252-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7f252-131">**Uso del controllo Media Player di Windows in una pagina Web**</span><span class="sxs-lookup"><span data-stu-id="7f252-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




