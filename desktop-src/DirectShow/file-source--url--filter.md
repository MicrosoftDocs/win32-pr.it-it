---
description: Filtro origine file (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro origine file (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909239"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="0c5e3-103">Filtro origine file (URL)</span><span class="sxs-lookup"><span data-stu-id="0c5e3-103">File Source (URL) Filter</span></span>

<span data-ttu-id="0c5e3-104">Il filtro origine file URL è un filtro di origine asincrono generico che funziona con qualsiasi file di origine che può essere identificato da un Uniform Resource Locator (URL) e il cui tipo di elemento multimediale principale è stream.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="0c5e3-105">Sono inclusi i file AVI, MOV, MPEG e WAV.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="0c5e3-106">Richiede che il filtro downstream sia un parser, ad esempio [mpeg-1 stream splitter,](mpeg-1-stream-splitter-filter.md) [AVI Splitter](avi-splitter-filter.md)o [QuickTime Movie Parser.](quicktime-movie-parser-filter.md)</span><span class="sxs-lookup"><span data-stu-id="0c5e3-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



| <span data-ttu-id="0c5e3-107">Label</span><span class="sxs-lookup"><span data-stu-id="0c5e3-107">Label</span></span> | <span data-ttu-id="0c5e3-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5e3-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5e3-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="0c5e3-109">Filter Interfaces</span></span>                        | <span data-ttu-id="0c5e3-110">[**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="0c5e3-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="0c5e3-111">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="0c5e3-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="0c5e3-112">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0c5e3-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="0c5e3-113">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="0c5e3-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0c5e3-114">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0c5e3-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="0c5e3-115">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="0c5e3-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="0c5e3-116">Flusso \_ MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-116">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="0c5e3-117">Il sottotipo dipende dal formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-117">The subtype depends on the media format.</span></span> <span data-ttu-id="0c5e3-118">(MEDIASUBTYPE \_ NULL se il filtro non riconosce il formato.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-118">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="0c5e3-119">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="0c5e3-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0c5e3-120">[**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="0c5e3-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="0c5e3-121">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="0c5e3-121">Filter CLSID</span></span>                             | <span data-ttu-id="0c5e3-122">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="0c5e3-122">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="0c5e3-123">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0c5e3-123">Property Page CLSID</span></span>                      | <span data-ttu-id="0c5e3-124">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0c5e3-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="0c5e3-125">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="0c5e3-125">Executable</span></span>                               | <span data-ttu-id="0c5e3-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0c5e3-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="0c5e3-127">Merito</span><span class="sxs-lookup"><span data-stu-id="0c5e3-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="0c5e3-128">MERITO \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="0c5e3-128">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="0c5e3-129">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="0c5e3-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0c5e3-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0c5e3-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0c5e3-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c5e3-131">Remarks</span></span>

<span data-ttu-id="0c5e3-132">Questo filtro usa URLMon e supporta le code pages.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-132">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c5e3-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c5e3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c5e3-134">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="0c5e3-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



