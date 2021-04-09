---
description: Filtro traversa video analogico
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro traversa video analogico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965641"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="8ee39-103">Filtro traversa video analogico</span><span class="sxs-lookup"><span data-stu-id="8ee39-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="8ee39-104">Il filtro traversa video analogico rappresenta una traversa video in un dispositivo di acquisizione video che supporta il Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="8ee39-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="8ee39-105">Questo filtro è un filtro wrapper per le barre multibarra nei dispositivi di streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="8ee39-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="8ee39-106">Il nome descrittivo del filtro viene ricavato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ee39-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="8ee39-107">Ogni pin di output rappresenta un percorso hardware per il video di Baseband analogico.</span><span class="sxs-lookup"><span data-stu-id="8ee39-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="8ee39-108">Uno dei pin di input deriva da un sintonizzatore TV (il [filtro del sintonizzatore TV](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="8ee39-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="8ee39-109">Altri pin di input supportano flussi video o audio.</span><span class="sxs-lookup"><span data-stu-id="8ee39-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="8ee39-110">Il filtro supporta eventuali sottotipi di supporti e formati supportati nelle connessioni downstream.</span><span class="sxs-lookup"><span data-stu-id="8ee39-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="8ee39-111">Non è possibile creare direttamente questo filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="8ee39-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="8ee39-112">L'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) aggiunge automaticamente questo filtro al grafico in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="8ee39-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="8ee39-113">Per ulteriori informazioni sui filtri wrapper e sui dispositivi di streaming WDM, vedere la pagina relativa al [modo in cui i dispositivi hardware partecipano al grafico dei filtri](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="8ee39-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee39-114">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="8ee39-114">Filter Interfaces</span></span>                        | <span data-ttu-id="8ee39-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="8ee39-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="8ee39-116">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="8ee39-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="8ee39-117">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="8ee39-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="8ee39-118">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="8ee39-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="8ee39-119">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="8ee39-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="8ee39-120">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="8ee39-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="8ee39-121">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="8ee39-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="8ee39-122">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="8ee39-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="8ee39-123">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="8ee39-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="8ee39-124">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="8ee39-124">Filter CLSID</span></span>                             | <span data-ttu-id="8ee39-125">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8ee39-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="8ee39-126">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8ee39-126">Property Page CLSID</span></span>                      | <span data-ttu-id="8ee39-127">\_CROSSBARFILTERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="8ee39-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="8ee39-128">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="8ee39-128">Executable</span></span>                               | <span data-ttu-id="8ee39-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="8ee39-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="8ee39-130">Merito</span><span class="sxs-lookup"><span data-stu-id="8ee39-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="8ee39-131">Dipendente dal driver.</span><span class="sxs-lookup"><span data-stu-id="8ee39-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="8ee39-132">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="8ee39-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8ee39-133">\_KSCATEGORY \_ traversa</span><span class="sxs-lookup"><span data-stu-id="8ee39-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="8ee39-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ee39-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ee39-135">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="8ee39-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="8ee39-136">Uso di maniglie</span><span class="sxs-lookup"><span data-stu-id="8ee39-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



