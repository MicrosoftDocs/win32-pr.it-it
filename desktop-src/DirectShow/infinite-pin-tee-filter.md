---
description: Filtro del Pin Tee infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro del Pin Tee infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401268"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="9c797-103">Filtro del Pin Tee infinito</span><span class="sxs-lookup"><span data-stu-id="9c797-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="9c797-104">Questo filtro recapita gli esempi recapitati al pin di input a un numero variabile di pin di output.</span><span class="sxs-lookup"><span data-stu-id="9c797-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="9c797-105">Quando viene creata un'istanza del filtro, è presente un pin di output.</span><span class="sxs-lookup"><span data-stu-id="9c797-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="9c797-106">Ogni volta che viene connesso un pin di output, il filtro crea un altro pin di output.</span><span class="sxs-lookup"><span data-stu-id="9c797-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="9c797-107">Tutti i pin di output condividono lo stesso tipo di supporto del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="9c797-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="9c797-108">Una versione di questo filtro viene fornita anche come esempio SDK.</span><span class="sxs-lookup"><span data-stu-id="9c797-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="9c797-109">Vedere l' [esempio di filtro InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9c797-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c797-110">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="9c797-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="9c797-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="9c797-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="9c797-112">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="9c797-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="9c797-113">Qualsiasi tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="9c797-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="9c797-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="9c797-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="9c797-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9c797-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="9c797-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="9c797-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="9c797-117">Qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="9c797-117">Any media type.</span></span> <span data-ttu-id="9c797-118">Il tipo di output corrisponde sempre al tipo di input, per tutti i pin di output</span><span class="sxs-lookup"><span data-stu-id="9c797-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="9c797-119">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="9c797-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="9c797-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9c797-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="9c797-121">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="9c797-121">Filter CLSID</span></span>                             | <span data-ttu-id="9c797-122">\_INFTEE CLSID</span><span class="sxs-lookup"><span data-stu-id="9c797-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="9c797-123">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9c797-123">Property Page CLSID</span></span>                      | <span data-ttu-id="9c797-124">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9c797-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="9c797-125">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="9c797-125">Executable</span></span>                               | <span data-ttu-id="9c797-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="9c797-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="9c797-127">Merito</span><span class="sxs-lookup"><span data-stu-id="9c797-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="9c797-128">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="9c797-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="9c797-129">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="9c797-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9c797-130">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="9c797-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="9c797-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c797-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c797-132">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c797-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



