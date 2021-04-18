---
title: Considerazioni sui mercati internazionali
description: Considerazioni sui mercati internazionali
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Negozi online di Windows Media Player, mercati internazionali
- negozi online, mercati internazionali
- digitare 1 negozi online, mercati internazionali
- digitare 2 negozi online, mercati internazionali
- mercati internazionali
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298471"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="ed691-113">Considerazioni sui mercati internazionali</span><span class="sxs-lookup"><span data-stu-id="ed691-113">Considerations for International Markets</span></span>

<span data-ttu-id="ed691-114">Se la società crea negozi online per più mercati, è necessario fornire a Microsoft l'URL di un documento ServiceInfo per ogni mercato.</span><span class="sxs-lookup"><span data-stu-id="ed691-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="ed691-115">Questa operazione può essere eseguita in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed691-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="ed691-116">Creare un documento ServiceInfo separato per ogni mercato.</span><span class="sxs-lookup"><span data-stu-id="ed691-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="ed691-117">In questo caso, è possibile fornire a Microsoft URL che puntano a singoli documenti ServiceInfo per ogni negozio online in ogni mercato.</span><span class="sxs-lookup"><span data-stu-id="ed691-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="ed691-118">Creare un singolo documento ServiceInfo per tutti i mercati.</span><span class="sxs-lookup"><span data-stu-id="ed691-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="ed691-119">Quando si esegue questa operazione, si fornisce a Microsoft lo stesso URL per ogni mercato.</span><span class="sxs-lookup"><span data-stu-id="ed691-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="ed691-120">Il documento ServiceInfo, creato come pagina ASP, può quindi rilevare dinamicamente la posizione dell'utente in base ai parametri della stringa di query.</span><span class="sxs-lookup"><span data-stu-id="ed691-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="ed691-121">Windows Media Player aggiunge una stringa di query alla richiesta dell'URL ServiceInfo che fornisce informazioni sulle impostazioni locali e sulla posizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ed691-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="ed691-122">Se il negozio online usa queste informazioni per determinare il contenuto da visualizzare, è necessario aggiungere i valori in modo dinamico ai propri URL nel documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="ed691-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="ed691-123">Questo è il modo migliore per assicurarsi che gli URL delle pagine Web contengano sempre i parametri previsti.</span><span class="sxs-lookup"><span data-stu-id="ed691-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="ed691-124">Dopo aver determinato la posizione e la preferenza per la lingua dell'utente, è possibile salvare in modo permanente le informazioni per le sessioni future.</span><span class="sxs-lookup"><span data-stu-id="ed691-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="ed691-125">A tale scopo, è possibile usare qualsiasi tecnica utilizzata in genere in una pagina Web, ad esempio cookie, oppure usando l'oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="ed691-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed691-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed691-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed691-127">**Creazione dinamica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ed691-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="ed691-128">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="ed691-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ed691-129">**Elemento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ed691-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 




