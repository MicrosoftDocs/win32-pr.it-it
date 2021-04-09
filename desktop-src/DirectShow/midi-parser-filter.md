---
description: Filtro del parser MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro del parser MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965485"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="61d4e-103">Filtro del parser MIDI</span><span class="sxs-lookup"><span data-stu-id="61d4e-103">MIDI Parser Filter</span></span>

<span data-ttu-id="61d4e-104">Il filtro del parser MIDI legge i dati MIDI presenti in. MID e. File RMI.</span><span class="sxs-lookup"><span data-stu-id="61d4e-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="61d4e-105">Il filtro accetta un flusso dall' [origine file asincrona](file-source--async--filter.md) o i filtri [origine file URL](file-source--url--filter.md) e restituisce esempi MIDI al [**renderer MIDI**](midi-renderer-filter.md) per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="61d4e-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d4e-106">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="61d4e-106">Filter Interfaces</span></span>                        | <span data-ttu-id="61d4e-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="61d4e-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="61d4e-108">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="61d4e-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="61d4e-109">\_Flusso MEDIATYPE, MEDIASUBTYPE \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="61d4e-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="61d4e-110">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="61d4e-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="61d4e-111">[**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="61d4e-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="61d4e-112">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="61d4e-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="61d4e-113">MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="61d4e-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="61d4e-114">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="61d4e-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="61d4e-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="61d4e-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="61d4e-116">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="61d4e-116">Filter CLSID</span></span>                             | <span data-ttu-id="61d4e-117">\_MIDIPARSER CLSID</span><span class="sxs-lookup"><span data-stu-id="61d4e-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="61d4e-118">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="61d4e-118">Property Page CLSID</span></span>                      | <span data-ttu-id="61d4e-119">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="61d4e-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="61d4e-120">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="61d4e-120">Executable</span></span>                               | <span data-ttu-id="61d4e-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="61d4e-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="61d4e-122">Merito</span><span class="sxs-lookup"><span data-stu-id="61d4e-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="61d4e-123">VALORE \_ improbabile</span><span class="sxs-lookup"><span data-stu-id="61d4e-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="61d4e-124">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="61d4e-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="61d4e-125">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="61d4e-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="61d4e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="61d4e-126">Remarks</span></span>

<span data-ttu-id="61d4e-127">Per altre informazioni, vedere [**renderer MIDI**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="61d4e-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61d4e-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61d4e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61d4e-129">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="61d4e-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



