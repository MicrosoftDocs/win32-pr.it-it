---
title: Integrazione degli acquisti per i negozi di tipo 2 online
description: Integrazione degli acquisti per i negozi di tipo 2 online
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Online Stores, Purchase Integration
- negozi online, integrazione degli acquisti
- digitare 2 negozi online, integrazione degli acquisti
- Windows Media Player Online Stores, integrazione degli acquisti
- negozi online, integrazione degli acquisti
- digitare 2 negozi online, integrazione degli acquisti
- Windows Media Player, integrazione degli acquisti
- Windows Media Player, integrazione degli acquisti
- integrazione degli acquisti
- integrazione di acquisti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298551"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="2bdb3-113">Integrazione degli acquisti per i negozi di tipo 2 online</span><span class="sxs-lookup"><span data-stu-id="2bdb3-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="2bdb3-114">Quando Windows Media Player riproduce contenuto multimediale digitale o l'utente sceglie **trova informazioni sugli album**, il lettore offre all'utente un collegamento per acquistare il CD o il DVD da cui è stato originato il contenuto se è disponibile un collegamento di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="2bdb3-115">Quando l'utente fa clic sul collegamento, Windows Media Player 10 o versioni successive chiama nell'archivio musica corrente per gestire la richiesta di acquisto.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="2bdb3-116">Quando si verifica questa situazione, il lettore passa al primo riquadro attività del servizio (in Windows Media Player 10) o alla scheda Online Stores (in Windows Media Player 11) e visualizza la pagina Web specificata dall'attributo **MediaPlayerURL** dell'elemento **BuyCD** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="2bdb3-117">Gli attributi **MediaCenterURL** e **BrowserURL** vengono utilizzati in modo analogo per gestire le chiamate da Windows xp Media Center Edition 2004 e Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="2bdb3-118">Windows Media Player aggiunge una stringa di query all'URL per fornire informazioni al negozio online sul contenuto che l'utente ha scelto di acquistare.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="2bdb3-119">La stringa di query include attributi come **title**, **album** e **Artist**, che possono essere usati dall'archivio online per determinare l'album corretto da vendere.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="2bdb3-120">La documentazione di riferimento per l'elemento **BuyCD** fornisce l'elenco completo degli attributi della stringa di query e le relative descrizioni.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="2bdb3-121">Linee guida per la pagina BuyCD</span><span class="sxs-lookup"><span data-stu-id="2bdb3-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="2bdb3-122">Quando si crea la pagina Web BuyCD, usare le linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bdb3-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="2bdb3-123">La pagina deve identificare chiaramente l'archivio online che fornisce le informazioni.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="2bdb3-124">A tale scopo, è possibile visualizzare in primo piano il logo, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="2bdb3-125">La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="2bdb3-126">È preferibile fornire le informazioni di acquisto iniziali senza richiedere all'utente di installare programmi o accedere al proprio negozio online.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bdb3-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bdb3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bdb3-128">**Informazioni sui negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="2bdb3-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2bdb3-129">**Elemento BuyCD**</span><span class="sxs-lookup"><span data-stu-id="2bdb3-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 




