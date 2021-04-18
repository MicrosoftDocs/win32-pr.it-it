---
title: Tipi percepiti (funzionalità legacy dell'ambiente Windows)
description: PerceivedType è una proprietà che classifica un elemento nell'indice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300898"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="24759-103">Tipi percepiti (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="24759-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="24759-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="24759-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="24759-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="24759-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="24759-106">`PerceivedType` è una proprietà che classifica un elemento nell'indice.</span><span class="sxs-lookup"><span data-stu-id="24759-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="24759-107">Questa classificazione è diversa dalla classificazione "Kind" usata dalla sintassi di [query avanzata](-search-2x-wds-aqsreference.md) ma consente agli utenti di affinare i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="24759-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="24759-108">Il tipo AQS consente agli utenti di limitare la query di ricerca mentre la proprietà PerceivedType consente agli utenti di filtrare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="24759-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="24759-109">Tipi</span><span class="sxs-lookup"><span data-stu-id="24759-109">Types</span></span>

<span data-ttu-id="24759-110">Utilizzare la proprietà PerceivedType per classificare il tipo di file in modo che gli utenti possano filtrare i risultati della ricerca in base al tipo.</span><span class="sxs-lookup"><span data-stu-id="24759-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="24759-111">L'output deve essere una delle stringhe seguenti:</span><span class="sxs-lookup"><span data-stu-id="24759-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="24759-112">contact</span><span class="sxs-lookup"><span data-stu-id="24759-112">contact</span></span>
-   <span data-ttu-id="24759-113">(DIP) interno</span><span class="sxs-lookup"><span data-stu-id="24759-113">communications</span></span>
-   <span data-ttu-id="24759-114">comunicazioni/posta elettronica</span><span class="sxs-lookup"><span data-stu-id="24759-114">communications/email</span></span>
-   <span data-ttu-id="24759-115">comunicazioni/calendario</span><span class="sxs-lookup"><span data-stu-id="24759-115">communications/calendar</span></span>
-   <span data-ttu-id="24759-116">comunicazioni/attività</span><span class="sxs-lookup"><span data-stu-id="24759-116">communications/task</span></span>
-   <span data-ttu-id="24759-117">comunicazioni/messaggistica immediata</span><span class="sxs-lookup"><span data-stu-id="24759-117">communications/im</span></span>
-   <span data-ttu-id="24759-118">documento</span><span class="sxs-lookup"><span data-stu-id="24759-118">document</span></span>
-   <span data-ttu-id="24759-119">documento/nota</span><span class="sxs-lookup"><span data-stu-id="24759-119">document/note</span></span>
-   <span data-ttu-id="24759-120">documento/testo</span><span class="sxs-lookup"><span data-stu-id="24759-120">document/text</span></span>
-   <span data-ttu-id="24759-121">documento/foglio di calcolo</span><span class="sxs-lookup"><span data-stu-id="24759-121">document/spreadsheet</span></span>
-   <span data-ttu-id="24759-122">documento/presentazione</span><span class="sxs-lookup"><span data-stu-id="24759-122">document/presentation</span></span>
-   <span data-ttu-id="24759-123">music</span><span class="sxs-lookup"><span data-stu-id="24759-123">music</span></span>
-   <span data-ttu-id="24759-124">images</span><span class="sxs-lookup"><span data-stu-id="24759-124">images</span></span>
-   <span data-ttu-id="24759-125">immagini/immagine</span><span class="sxs-lookup"><span data-stu-id="24759-125">images/picture</span></span>
-   <span data-ttu-id="24759-126">immagini/video</span><span class="sxs-lookup"><span data-stu-id="24759-126">images/video</span></span>
-   <span data-ttu-id="24759-127">folder</span><span class="sxs-lookup"><span data-stu-id="24759-127">folder</span></span>
-   <span data-ttu-id="24759-128">programma</span><span class="sxs-lookup"><span data-stu-id="24759-128">program</span></span>

<span data-ttu-id="24759-129">Ad esempio, quando si desidera creare un componente aggiuntivo filtro per un nuovo tipo di file immagine, è necessario implementare quanto segue nell'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):</span><span class="sxs-lookup"><span data-stu-id="24759-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="24759-130">**GetChunk** per restituire un FULLPROPSPEC che include: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span><span class="sxs-lookup"><span data-stu-id="24759-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="24759-131">**GetValue** per restituire un PROPVARIANT che include: VT \_ LPWSTR = "immagini/immagine"</span><span class="sxs-lookup"><span data-stu-id="24759-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="24759-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24759-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24759-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="24759-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24759-134">Sviluppo di componenti aggiuntivi IFilter</span><span class="sxs-lookup"><span data-stu-id="24759-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="24759-135">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="24759-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="24759-136">Sintassi di ricerca avanzata</span><span class="sxs-lookup"><span data-stu-id="24759-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="24759-137">SchemaTable</span><span class="sxs-lookup"><span data-stu-id="24759-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
