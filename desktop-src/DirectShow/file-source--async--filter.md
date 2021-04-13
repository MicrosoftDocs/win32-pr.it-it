---
description: Filtro di origine file (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro di origine file (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481645"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="d5cdb-103">Filtro di origine file (Async)</span><span class="sxs-lookup"><span data-stu-id="d5cdb-103">File Source (Async) Filter</span></span>

<span data-ttu-id="d5cdb-104">Il filtro origine file asincrono apre e legge i file locali di molti formati dati diversi e passa i dati a un filtro del parser.</span><span class="sxs-lookup"><span data-stu-id="d5cdb-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="d5cdb-105">Per scaricare i file multimediali dal Web tramite HTTP, usare il filtro di [origine file (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cdb-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="d5cdb-106">Per leggere i file ASF, usare il filtro [WM ASF Reader](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cdb-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cdb-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="d5cdb-107">Filter Interfaces</span></span>                        | <span data-ttu-id="d5cdb-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="d5cdb-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="d5cdb-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="d5cdb-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="d5cdb-110">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="d5cdb-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="d5cdb-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="d5cdb-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d5cdb-112">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="d5cdb-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="d5cdb-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="d5cdb-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="d5cdb-114">**MEDIATYPE \_ Flusso**.</span><span class="sxs-lookup"><span data-stu-id="d5cdb-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="d5cdb-115">Il sottotipo dipende dal formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="d5cdb-115">The subtype depends on the media format.</span></span> <span data-ttu-id="d5cdb-116">(**MEDIASUBTYPE \_ null** se il filtro non riconosce il formato).</span><span class="sxs-lookup"><span data-stu-id="d5cdb-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="d5cdb-117">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="d5cdb-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d5cdb-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="d5cdb-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="d5cdb-119">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="d5cdb-119">Filter CLSID</span></span>                             | <span data-ttu-id="d5cdb-120">**\_ASYNCREADER CLSID**</span><span class="sxs-lookup"><span data-stu-id="d5cdb-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="d5cdb-121">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d5cdb-121">Property Page CLSID</span></span>                      | <span data-ttu-id="d5cdb-122">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d5cdb-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="d5cdb-123">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="d5cdb-123">Executable</span></span>                               | <span data-ttu-id="d5cdb-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d5cdb-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="d5cdb-125">Merito</span><span class="sxs-lookup"><span data-stu-id="d5cdb-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="d5cdb-126">**VALORE \_ improbabile**</span><span class="sxs-lookup"><span data-stu-id="d5cdb-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="d5cdb-127">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="d5cdb-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d5cdb-128">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="d5cdb-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="d5cdb-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5cdb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5cdb-130">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5cdb-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



