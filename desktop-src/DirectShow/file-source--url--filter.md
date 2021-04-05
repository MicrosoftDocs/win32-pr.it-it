---
description: Filtro origine file (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro origine file (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125106"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="db5e5-103">Filtro origine file (URL)</span><span class="sxs-lookup"><span data-stu-id="db5e5-103">File Source (URL) Filter</span></span>

<span data-ttu-id="db5e5-104">Il filtro origine file URL è un filtro di origine asincrono generico che funziona con qualsiasi file di origine che può essere identificato da un Uniform Resource Locator (URL) e il cui tipo di supporto principale è flusso.</span><span class="sxs-lookup"><span data-stu-id="db5e5-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="db5e5-105">Sono inclusi i file AVI, MOV, MPEG e WAV.</span><span class="sxs-lookup"><span data-stu-id="db5e5-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="db5e5-106">È necessario che il filtro downstream sia un parser, ad esempio il [separatore di flusso MPEG-1](mpeg-1-stream-splitter-filter.md), il [separatore AVI](avi-splitter-filter.md)o il [parser film QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="db5e5-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db5e5-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="db5e5-107">Filter Interfaces</span></span>                        | <span data-ttu-id="db5e5-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="db5e5-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="db5e5-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="db5e5-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="db5e5-110">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="db5e5-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="db5e5-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="db5e5-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="db5e5-112">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="db5e5-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="db5e5-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="db5e5-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="db5e5-114">\_Flusso MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="db5e5-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="db5e5-115">Il sottotipo dipende dal formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="db5e5-115">The subtype depends on the media format.</span></span> <span data-ttu-id="db5e5-116">(MEDIASUBTYPE \_ NULL se il filtro non riconosce il formato.</span><span class="sxs-lookup"><span data-stu-id="db5e5-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="db5e5-117">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="db5e5-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="db5e5-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="db5e5-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="db5e5-119">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="db5e5-119">Filter CLSID</span></span>                             | <span data-ttu-id="db5e5-120">\_URLREADER CLSID</span><span class="sxs-lookup"><span data-stu-id="db5e5-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="db5e5-121">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="db5e5-121">Property Page CLSID</span></span>                      | <span data-ttu-id="db5e5-122">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="db5e5-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="db5e5-123">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="db5e5-123">Executable</span></span>                               | <span data-ttu-id="db5e5-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="db5e5-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="db5e5-125">Merito</span><span class="sxs-lookup"><span data-stu-id="db5e5-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="db5e5-126">VALORE \_ improbabile</span><span class="sxs-lookup"><span data-stu-id="db5e5-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="db5e5-127">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="db5e5-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="db5e5-128">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="db5e5-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="db5e5-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="db5e5-129">Remarks</span></span>

<span data-ttu-id="db5e5-130">Questo filtro usa URLMon e supporta le tabelle codici.</span><span class="sxs-lookup"><span data-stu-id="db5e5-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db5e5-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db5e5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db5e5-132">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="db5e5-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



