---
description: Filtro barra incrociata video analogico
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro barra incrociata video analogico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909599"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="e48ce-103">Filtro barra incrociata video analogico</span><span class="sxs-lookup"><span data-stu-id="e48ce-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="e48ce-104">Il filtro crossbar video analogico rappresenta una barra incrociata video in un dispositivo di acquisizione video che supporta Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="e48ce-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="e48ce-105">Questo filtro è un filtro wrapper per le barre incrociate nei dispositivi di streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="e48ce-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="e48ce-106">Il nome descrittivo del filtro deriva dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e48ce-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="e48ce-107">Ogni pin di output rappresenta un percorso hardware per video di baseband analogico.</span><span class="sxs-lookup"><span data-stu-id="e48ce-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="e48ce-108">Uno dei pin di input proviene da un siner TV [(TV Tuner Filter).](tv-tuner-filter.md)</span><span class="sxs-lookup"><span data-stu-id="e48ce-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="e48ce-109">Altri pin di input supportano flussi audio o video.</span><span class="sxs-lookup"><span data-stu-id="e48ce-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="e48ce-110">Il filtro supporta tutti i sottotipi multimediali e i formati supportati nelle connessioni downstream.</span><span class="sxs-lookup"><span data-stu-id="e48ce-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="e48ce-111">Non è possibile creare direttamente questo filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="e48ce-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="e48ce-112">[**L'interfaccia ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) aggiunge automaticamente questo filtro al grafo in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="e48ce-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="e48ce-113">Per altre informazioni sui filtri wrapper e sui dispositivi di streaming WDM, vedere [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e48ce-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



| <span data-ttu-id="e48ce-114">Label</span><span class="sxs-lookup"><span data-stu-id="e48ce-114">Label</span></span> | <span data-ttu-id="e48ce-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e48ce-115">Value</span></span> |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e48ce-116">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="e48ce-116">Filter Interfaces</span></span>                        | <span data-ttu-id="e48ce-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="e48ce-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="e48ce-118">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="e48ce-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="e48ce-119">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="e48ce-119">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="e48ce-120">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="e48ce-120">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="e48ce-121">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="e48ce-121">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="e48ce-122">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="e48ce-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="e48ce-123">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="e48ce-123">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="e48ce-124">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="e48ce-124">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="e48ce-125">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="e48ce-125">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="e48ce-126">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="e48ce-126">Filter CLSID</span></span>                             | <span data-ttu-id="e48ce-127">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e48ce-127">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="e48ce-128">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="e48ce-128">Property Page CLSID</span></span>                      | <span data-ttu-id="e48ce-129">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="e48ce-129">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="e48ce-130">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="e48ce-130">Executable</span></span>                               | <span data-ttu-id="e48ce-131">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="e48ce-131">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="e48ce-132">Merito</span><span class="sxs-lookup"><span data-stu-id="e48ce-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="e48ce-133">Dipendente dal driver.</span><span class="sxs-lookup"><span data-stu-id="e48ce-133">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="e48ce-134">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="e48ce-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e48ce-135">AM \_ KSCATEGORY \_ CROSSBAR</span><span class="sxs-lookup"><span data-stu-id="e48ce-135">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="e48ce-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e48ce-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e48ce-137">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="e48ce-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="e48ce-138">Uso delle barre incrociate</span><span class="sxs-lookup"><span data-stu-id="e48ce-138">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



