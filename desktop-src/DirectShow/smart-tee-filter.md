---
description: Filtro Smart Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909299"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="af5ce-103">Filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="af5ce-103">Smart Tee Filter</span></span>

<span data-ttu-id="af5ce-104">Il filtro Smart Tee viene usato nei grafici di acquisizione video per suddividere il flusso video in un flusso di anteprima e un flusso di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="af5ce-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="af5ce-105">Questa operazione viene eseguita senza alcuna copia aggiuntiva dei dati.</span><span class="sxs-lookup"><span data-stu-id="af5ce-105">This is done without any additional data copying.</span></span> <span data-ttu-id="af5ce-106">I pin di output supportano qualsiasi tipo di supporto supportato nella connessione downstream.</span><span class="sxs-lookup"><span data-stu-id="af5ce-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="af5ce-107">Il filtro Smart Tee è utile quando un filtro di acquisizione video non fornisce pin separati per l'acquisizione e l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="af5ce-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="af5ce-108">Il filtro Smart Tee fornisce i dati di anteprima solo se questa operazione non influisce sulle prestazioni di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="af5ce-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="af5ce-109">Rimuove anche i timestamp dal flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="af5ce-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="af5ce-110">Il generatore di grafi di acquisizione inserisce automaticamente il filtro Smart Tee quando necessario.</span><span class="sxs-lookup"><span data-stu-id="af5ce-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="af5ce-111">Per altre informazioni, vedere [Combinazione di acquisizione video e anteprima.](combining-video-capture-and-preview.md)</span><span class="sxs-lookup"><span data-stu-id="af5ce-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="af5ce-112">La figura seguente mostra un tipico grafico di acquisizione che usa il filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="af5ce-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![uso del filtro Smart Tee](images/smarttee.png)



| <span data-ttu-id="af5ce-114">Label</span><span class="sxs-lookup"><span data-stu-id="af5ce-114">Label</span></span> | <span data-ttu-id="af5ce-115">Valore</span><span class="sxs-lookup"><span data-stu-id="af5ce-115">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af5ce-116">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="af5ce-116">Filter Interfaces</span></span>                        | [<span data-ttu-id="af5ce-117">**Filtro IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="af5ce-117">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="af5ce-118">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="af5ce-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="af5ce-119">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="af5ce-119">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="af5ce-120">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="af5ce-120">Input Pin Interfaces</span></span>                     | <span data-ttu-id="af5ce-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="af5ce-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="af5ce-122">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="af5ce-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="af5ce-123">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="af5ce-123">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="af5ce-124">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="af5ce-124">Output Pin Interfaces</span></span>                    | <span data-ttu-id="af5ce-125">[**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="af5ce-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="af5ce-126">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="af5ce-126">Filter CLSID</span></span>                             | <span data-ttu-id="af5ce-127">CLSID \_ SmartTee</span><span class="sxs-lookup"><span data-stu-id="af5ce-127">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="af5ce-128">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="af5ce-128">Property Page CLSID</span></span>                      | <span data-ttu-id="af5ce-129">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="af5ce-129">No property page.</span></span>                                                                                              |
| <span data-ttu-id="af5ce-130">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="af5ce-130">Executable</span></span>                               | <span data-ttu-id="af5ce-131">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="af5ce-131">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="af5ce-132">Merito</span><span class="sxs-lookup"><span data-stu-id="af5ce-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="af5ce-133">MERITO \_ NON \_ \_ USARE</span><span class="sxs-lookup"><span data-stu-id="af5ce-133">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="af5ce-134">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="af5ce-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="af5ce-135">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="af5ce-135">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="af5ce-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="af5ce-136">Remarks</span></span>

<span data-ttu-id="af5ce-137">Il pin di acquisizione è il pin di output 0 e il pin di anteprima è il pin di output 1.</span><span class="sxs-lookup"><span data-stu-id="af5ce-137">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af5ce-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af5ce-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af5ce-139">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="af5ce-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



