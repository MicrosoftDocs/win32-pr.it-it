---
description: Filtro tee per pin infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro tee Perni infiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909229"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="36ef4-103">Filtro tee per pin infinito</span><span class="sxs-lookup"><span data-stu-id="36ef4-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="36ef4-104">Questo filtro recapita gli esempi recapitati al pin di input a un numero variabile di pin di output.</span><span class="sxs-lookup"><span data-stu-id="36ef4-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="36ef4-105">Quando viene creata un'istanza del filtro, ha un pin di output.</span><span class="sxs-lookup"><span data-stu-id="36ef4-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="36ef4-106">Ogni volta che un pin di output è connesso, il filtro crea un altro pin di output.</span><span class="sxs-lookup"><span data-stu-id="36ef4-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="36ef4-107">Tutti i pin di output condividono lo stesso tipo di supporto del pin di input.</span><span class="sxs-lookup"><span data-stu-id="36ef4-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="36ef4-108">Una versione di questo filtro viene fornita anche come esempio sdk.</span><span class="sxs-lookup"><span data-stu-id="36ef4-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="36ef4-109">Vedere [Esempio di filtro InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="36ef4-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="36ef4-110">Label</span><span class="sxs-lookup"><span data-stu-id="36ef4-110">Label</span></span> | <span data-ttu-id="36ef4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="36ef4-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ef4-112">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="36ef4-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="36ef4-113">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="36ef4-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="36ef4-114">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="36ef4-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="36ef4-115">Qualsiasi tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="36ef4-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="36ef4-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="36ef4-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="36ef4-117">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="36ef4-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="36ef4-118">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="36ef4-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="36ef4-119">Qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="36ef4-119">Any media type.</span></span> <span data-ttu-id="36ef4-120">Il tipo di output corrisponde sempre al tipo di input, per tutti i pin di output</span><span class="sxs-lookup"><span data-stu-id="36ef4-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="36ef4-121">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="36ef4-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="36ef4-122">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="36ef4-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="36ef4-123">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="36ef4-123">Filter CLSID</span></span>                             | <span data-ttu-id="36ef4-124">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="36ef4-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="36ef4-125">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="36ef4-125">Property Page CLSID</span></span>                      | <span data-ttu-id="36ef4-126">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="36ef4-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="36ef4-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="36ef4-127">Executable</span></span>                               | <span data-ttu-id="36ef4-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="36ef4-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="36ef4-129">Merito</span><span class="sxs-lookup"><span data-stu-id="36ef4-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="36ef4-130">NON \_ \_ USARE \_</span><span class="sxs-lookup"><span data-stu-id="36ef4-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="36ef4-131">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="36ef4-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="36ef4-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="36ef4-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="36ef4-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36ef4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36ef4-134">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="36ef4-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



