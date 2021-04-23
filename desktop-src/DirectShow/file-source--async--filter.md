---
description: Filtro origine file (asincrono)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro origine file (asincrono)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909699"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="4b95c-103">Filtro origine file (asincrono)</span><span class="sxs-lookup"><span data-stu-id="4b95c-103">File Source (Async) Filter</span></span>

<span data-ttu-id="4b95c-104">Il filtro Origine file asincrona apre e legge i file locali di molti formati di dati diversi e passa i dati a un filtro del parser.</span><span class="sxs-lookup"><span data-stu-id="4b95c-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="4b95c-105">Per scaricare file multimediali dal Web tramite HTTP, usare il filtro [Origine file (URL).](file-source--url--filter.md)</span><span class="sxs-lookup"><span data-stu-id="4b95c-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="4b95c-106">Per leggere i file ASF, usare il filtro [Lettore ASF WM.](wm-asf-reader-filter.md)</span><span class="sxs-lookup"><span data-stu-id="4b95c-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="4b95c-107">Label</span><span class="sxs-lookup"><span data-stu-id="4b95c-107">Label</span></span> | <span data-ttu-id="4b95c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4b95c-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b95c-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="4b95c-109">Filter Interfaces</span></span>                        | <span data-ttu-id="4b95c-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="4b95c-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="4b95c-111">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="4b95c-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="4b95c-112">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="4b95c-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="4b95c-113">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="4b95c-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="4b95c-114">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="4b95c-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="4b95c-115">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="4b95c-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="4b95c-116">**MEDIATYPE \_ Flusso**.</span><span class="sxs-lookup"><span data-stu-id="4b95c-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="4b95c-117">Il sottotipo dipende dal formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="4b95c-117">The subtype depends on the media format.</span></span> <span data-ttu-id="4b95c-118">(**MEDIASUBTYPE \_ NULL** se il filtro non riconosce il formato).</span><span class="sxs-lookup"><span data-stu-id="4b95c-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="4b95c-119">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="4b95c-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="4b95c-120">[**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="4b95c-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="4b95c-121">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="4b95c-121">Filter CLSID</span></span>                             | <span data-ttu-id="4b95c-122">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="4b95c-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="4b95c-123">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="4b95c-123">Property Page CLSID</span></span>                      | <span data-ttu-id="4b95c-124">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="4b95c-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="4b95c-125">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="4b95c-125">Executable</span></span>                               | <span data-ttu-id="4b95c-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="4b95c-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="4b95c-127">Merito</span><span class="sxs-lookup"><span data-stu-id="4b95c-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="4b95c-128">**MERITO \_ IMPROBABILE**</span><span class="sxs-lookup"><span data-stu-id="4b95c-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="4b95c-129">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="4b95c-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4b95c-130">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="4b95c-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="4b95c-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b95c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b95c-132">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="4b95c-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



