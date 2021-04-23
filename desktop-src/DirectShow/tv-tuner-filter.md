---
description: Filtro siner TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro siner TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909029"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="0d270-103">Filtro siner TV</span><span class="sxs-lookup"><span data-stu-id="0d270-103">TV Tuner Filter</span></span>

<span data-ttu-id="0d270-104">Il filtro Siner TV seleziona una trasmissione o un canale via cavo analogico da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="0d270-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="0d270-105">Il flusso di output singolo è un percorso hardware per video con banda di base analogica.</span><span class="sxs-lookup"><span data-stu-id="0d270-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="0d270-106">Questo output deve connettersi al filtro crossbar video analogico.</span><span class="sxs-lookup"><span data-stu-id="0d270-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="0d270-107">I pin di input includono un input per il cavo e un input dell'antenna.</span><span class="sxs-lookup"><span data-stu-id="0d270-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="0d270-108">Label</span><span class="sxs-lookup"><span data-stu-id="0d270-108">Label</span></span> | <span data-ttu-id="0d270-109">Valore</span><span class="sxs-lookup"><span data-stu-id="0d270-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d270-110">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="0d270-110">Filter Interfaces</span></span>                        | <span data-ttu-id="0d270-111">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject,** [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="0d270-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="0d270-112">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="0d270-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="0d270-113">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d270-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="0d270-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="0d270-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0d270-115">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d270-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="0d270-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="0d270-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="0d270-117">Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="0d270-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="0d270-118">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="0d270-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="0d270-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="0d270-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="0d270-120">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="0d270-120">Filter CLSID</span></span>                             | <span data-ttu-id="0d270-121">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="0d270-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="0d270-122">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0d270-122">Property Page CLSID</span></span>                      | <span data-ttu-id="0d270-123">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="0d270-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d270-124">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="0d270-124">Executable</span></span>                               | <span data-ttu-id="0d270-125">Kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="0d270-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="0d270-126">Merito</span><span class="sxs-lookup"><span data-stu-id="0d270-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="0d270-127">NON \_ \_ USARE \_</span><span class="sxs-lookup"><span data-stu-id="0d270-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="0d270-128">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="0d270-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0d270-129">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="0d270-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="0d270-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d270-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d270-131">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="0d270-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



