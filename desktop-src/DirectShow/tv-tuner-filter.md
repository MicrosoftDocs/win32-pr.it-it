---
description: Filtro sintonizzatore TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro sintonizzatore TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348556"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="cbfac-103">Filtro sintonizzatore TV</span><span class="sxs-lookup"><span data-stu-id="cbfac-103">TV Tuner Filter</span></span>

<span data-ttu-id="cbfac-104">Il filtro del sintonizzatore TV seleziona un canale di trasmissione o trasmissione analogo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="cbfac-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="cbfac-105">Il flusso di output singolo è un percorso hardware per il video di Baseband analogico.</span><span class="sxs-lookup"><span data-stu-id="cbfac-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="cbfac-106">Questo output deve connettersi al filtro per la traversa video analogo.</span><span class="sxs-lookup"><span data-stu-id="cbfac-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="cbfac-107">I pin di input includono un input per il cavo e un input di antenna.</span><span class="sxs-lookup"><span data-stu-id="cbfac-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfac-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="cbfac-108">Filter Interfaces</span></span>                        | <span data-ttu-id="cbfac-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**Impossibile IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="cbfac-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="cbfac-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="cbfac-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="cbfac-111">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="cbfac-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="cbfac-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="cbfac-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="cbfac-113">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="cbfac-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="cbfac-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="cbfac-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="cbfac-115">Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SubType \_ None audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="cbfac-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="cbfac-116">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="cbfac-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="cbfac-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="cbfac-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="cbfac-118">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="cbfac-118">Filter CLSID</span></span>                             | <span data-ttu-id="cbfac-119">\_TVTUNERFILTER CLSID</span><span class="sxs-lookup"><span data-stu-id="cbfac-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="cbfac-120">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="cbfac-120">Property Page CLSID</span></span>                      | <span data-ttu-id="cbfac-121">\_TVTUNERFILTERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="cbfac-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="cbfac-122">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="cbfac-122">Executable</span></span>                               | <span data-ttu-id="cbfac-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="cbfac-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="cbfac-124">Merito</span><span class="sxs-lookup"><span data-stu-id="cbfac-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="cbfac-125">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="cbfac-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="cbfac-126">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="cbfac-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cbfac-127">\_TVTUNER KSCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="cbfac-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="cbfac-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbfac-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbfac-129">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="cbfac-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



