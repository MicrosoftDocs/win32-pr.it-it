---
title: Integrazione delle informazioni sugli album
description: Integrazione delle informazioni sugli album
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online Stores, integrazione delle informazioni sugli album
- archivi online, integrazione delle informazioni sugli album
- digitare 2 archivi online, integrazione delle informazioni sugli album
- Windows Media Player Online Stores, integrazione delle informazioni sugli album
- negozi online, integrazione delle informazioni sugli album
- digitare 2 archivi online, integrazione delle informazioni sugli album
- Windows Media Player, integrazione delle informazioni sugli album
- Windows Media Player, integrazione delle informazioni sugli album
- integrazione delle informazioni sugli album
- integrazione delle informazioni sugli album
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044633"
---
# <a name="album-info-integration"></a><span data-ttu-id="8f3df-113">Integrazione delle informazioni sugli album</span><span class="sxs-lookup"><span data-stu-id="8f3df-113">Album Info Integration</span></span>

<span data-ttu-id="8f3df-114">Windows Media Player consente agli utenti di richiedere informazioni dettagliate sul CD o sul DVD da cui è stato originato il contenuto multimediale digitale facendo clic su un pulsante, ad esempio **altre informazioni**.</span><span class="sxs-lookup"><span data-stu-id="8f3df-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="8f3df-115">Quando l'utente fa clic sul pulsante, Windows Media Player 10 o versioni successive chiama nell'archivio musica corrente per visualizzare i dettagli dell'album.</span><span class="sxs-lookup"><span data-stu-id="8f3df-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="8f3df-116">Quando si verifica questa situazione, il lettore apre il riquadro informazioni album e visualizza la pagina Web specificata dall'attributo **URL** dell'elemento **AlbumInfo** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="8f3df-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="8f3df-117">Windows Media Player aggiunge una stringa di query all'URL per fornire informazioni al negozio online sul contenuto richiesto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8f3df-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="8f3df-118">La stringa di query include attributi come **title**, **album** e **Artist**, che possono essere usati dall'archivio online per determinare l'album corretto da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8f3df-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="8f3df-119">La documentazione di riferimento per l'elemento **AlbumInfo** fornisce l'elenco completo degli attributi della stringa di query e le relative descrizioni.</span><span class="sxs-lookup"><span data-stu-id="8f3df-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="8f3df-120">Linee guida per le informazioni sugli album</span><span class="sxs-lookup"><span data-stu-id="8f3df-120">Guidelines for Album Info</span></span>

<span data-ttu-id="8f3df-121">Quando si crea la pagina Web relativa alle informazioni sugli album, attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f3df-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="8f3df-122">La pagina deve identificare chiaramente l'archivio online che fornisce le informazioni.</span><span class="sxs-lookup"><span data-stu-id="8f3df-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="8f3df-123">A tale scopo, è possibile visualizzare in primo piano il logo, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="8f3df-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="8f3df-124">La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="8f3df-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="8f3df-125">Quando possibile, evitare l'esplorazione delle pagine all'interno della funzionalità informazioni sugli album.</span><span class="sxs-lookup"><span data-stu-id="8f3df-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="8f3df-126">Per la maggior parte delle attività, è necessario passare all'archivio online.</span><span class="sxs-lookup"><span data-stu-id="8f3df-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="8f3df-127">Si consiglia di fornire informazioni utili senza richiedere all'utente di installare programmi o accedere al proprio negozio online.</span><span class="sxs-lookup"><span data-stu-id="8f3df-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f3df-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f3df-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f3df-129">**Informazioni sui negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="8f3df-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8f3df-130">**Elemento AlbumInfo**</span><span class="sxs-lookup"><span data-stu-id="8f3df-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 




