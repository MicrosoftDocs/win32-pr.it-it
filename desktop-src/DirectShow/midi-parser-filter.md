---
description: Filtro parser MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro parser MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908429"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="fcc31-103">Filtro del parser MIDI</span><span class="sxs-lookup"><span data-stu-id="fcc31-103">MIDI Parser Filter</span></span>

<span data-ttu-id="fcc31-104">Il filtro midi parser legge i dati MIDI trovati in . MID e . File RMI.</span><span class="sxs-lookup"><span data-stu-id="fcc31-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="fcc31-105">Il filtro accetta un flusso dai filtri [Origine file](file-source--async--filter.md) asincrona o Origine [file URL](file-source--url--filter.md) e restituisce gli esempi MIDI al [**renderer MIDI**](midi-renderer-filter.md) per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="fcc31-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="fcc31-106">Label</span><span class="sxs-lookup"><span data-stu-id="fcc31-106">Label</span></span> | <span data-ttu-id="fcc31-107">Valore</span><span class="sxs-lookup"><span data-stu-id="fcc31-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc31-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="fcc31-108">Filter Interfaces</span></span>                        | <span data-ttu-id="fcc31-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="fcc31-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="fcc31-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="fcc31-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="fcc31-111">Flusso \_ MEDIATYPE, MEDIASUBTYPE \_ Midi</span><span class="sxs-lookup"><span data-stu-id="fcc31-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="fcc31-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="fcc31-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="fcc31-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="fcc31-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="fcc31-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="fcc31-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="fcc31-115">MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="fcc31-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="fcc31-116">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="fcc31-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="fcc31-117">[**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="fcc31-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="fcc31-118">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="fcc31-118">Filter CLSID</span></span>                             | <span data-ttu-id="fcc31-119">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="fcc31-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="fcc31-120">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="fcc31-120">Property Page CLSID</span></span>                      | <span data-ttu-id="fcc31-121">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="fcc31-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="fcc31-122">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="fcc31-122">Executable</span></span>                               | <span data-ttu-id="fcc31-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="fcc31-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="fcc31-124">Merito</span><span class="sxs-lookup"><span data-stu-id="fcc31-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="fcc31-125">PROBABILITÀ \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="fcc31-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="fcc31-126">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="fcc31-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="fcc31-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="fcc31-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="fcc31-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcc31-128">Remarks</span></span>

<span data-ttu-id="fcc31-129">Per altre informazioni, vedere [**Renderer MIDI.**](midi-renderer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="fcc31-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcc31-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fcc31-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcc31-131">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="fcc31-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



