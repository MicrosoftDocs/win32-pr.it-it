---
description: Filtro Smart Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482300"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="bca96-103">Filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="bca96-103">Smart Tee Filter</span></span>

<span data-ttu-id="bca96-104">Il filtro Smart Tee viene usato nei grafici di acquisizione video per suddividere il flusso video in un flusso di anteprima e in un flusso di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bca96-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="bca96-105">Questa operazione viene eseguita senza ulteriori operazioni di copia dei dati.</span><span class="sxs-lookup"><span data-stu-id="bca96-105">This is done without any additional data copying.</span></span> <span data-ttu-id="bca96-106">I pin di output supportano tutti i tipi di supporto supportati nella connessione downstream.</span><span class="sxs-lookup"><span data-stu-id="bca96-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="bca96-107">Il filtro Smart Tee è utile quando un filtro di acquisizione video non fornisce pin distinti per l'acquisizione e l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="bca96-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="bca96-108">Il filtro Smart Tee recapita i dati di anteprima solo se questa operazione non danneggia le prestazioni di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bca96-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="bca96-109">Consente inoltre di rimuovere gli indicatori temporali dal flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="bca96-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="bca96-110">Il generatore del grafico di acquisizione inserisce automaticamente il filtro di Smart Tee quando necessario.</span><span class="sxs-lookup"><span data-stu-id="bca96-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="bca96-111">Per altre informazioni, vedere [combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="bca96-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="bca96-112">Nella figura seguente viene illustrato un tipico grafico di acquisizione che utilizza il filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="bca96-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![uso del filtro Smart Tee](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca96-114">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="bca96-114">Filter Interfaces</span></span>                        | [<span data-ttu-id="bca96-115">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="bca96-115">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="bca96-116">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="bca96-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="bca96-117">MEDIATYPE \_ video, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="bca96-117">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="bca96-118">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="bca96-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="bca96-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="bca96-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="bca96-120">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="bca96-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="bca96-121">MEDIATYPE \_ video, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="bca96-121">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="bca96-122">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="bca96-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="bca96-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="bca96-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="bca96-124">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="bca96-124">Filter CLSID</span></span>                             | <span data-ttu-id="bca96-125">\_SMARTTEE CLSID</span><span class="sxs-lookup"><span data-stu-id="bca96-125">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="bca96-126">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="bca96-126">Property Page CLSID</span></span>                      | <span data-ttu-id="bca96-127">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bca96-127">No property page.</span></span>                                                                                              |
| <span data-ttu-id="bca96-128">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="bca96-128">Executable</span></span>                               | <span data-ttu-id="bca96-129">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="bca96-129">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="bca96-130">Merito</span><span class="sxs-lookup"><span data-stu-id="bca96-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="bca96-131">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="bca96-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="bca96-132">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="bca96-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="bca96-133">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="bca96-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="bca96-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="bca96-134">Remarks</span></span>

<span data-ttu-id="bca96-135">Il pin di acquisizione è il pin di output 0 e il pin di anteprima è il pin di output 1.</span><span class="sxs-lookup"><span data-stu-id="bca96-135">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bca96-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bca96-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca96-137">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="bca96-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



