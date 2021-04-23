---
description: Filtro VGA 16 Color Ditherer
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro VGA 16 Color Ditherer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908679"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="0ef81-103">Filtro VGA 16 Color Ditherer</span><span class="sxs-lookup"><span data-stu-id="0ef81-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="0ef81-104">Il filtro VGA 16 Color Ditherer esegue la conversione da un tipo di colore RGB a uno schermo a colori a 4 bit in modo che i flussi video AVI e MPEG possano essere visualizzati su monitor a 16 colori meno recenti.</span><span class="sxs-lookup"><span data-stu-id="0ef81-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="0ef81-105">Questo filtro viene inserito nel grafico tra un filtro decompressore e un filtro del renderer video.</span><span class="sxs-lookup"><span data-stu-id="0ef81-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="0ef81-106">Label</span><span class="sxs-lookup"><span data-stu-id="0ef81-106">Label</span></span> | <span data-ttu-id="0ef81-107">Valore</span><span class="sxs-lookup"><span data-stu-id="0ef81-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef81-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="0ef81-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="0ef81-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="0ef81-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="0ef81-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="0ef81-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="0ef81-111">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="0ef81-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="0ef81-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="0ef81-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0ef81-113">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0ef81-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="0ef81-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="0ef81-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="0ef81-115">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="0ef81-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="0ef81-116">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="0ef81-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0ef81-117">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0ef81-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="0ef81-118">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="0ef81-118">Filter CLSID</span></span>                             | <span data-ttu-id="0ef81-119">Dithering CLSID \_</span><span class="sxs-lookup"><span data-stu-id="0ef81-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="0ef81-120">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0ef81-120">Property Page CLSID</span></span>                      | <span data-ttu-id="0ef81-121">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ef81-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="0ef81-122">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="0ef81-122">Executable</span></span>                               | <span data-ttu-id="0ef81-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0ef81-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="0ef81-124">Merito</span><span class="sxs-lookup"><span data-stu-id="0ef81-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="0ef81-125">PROBABILITÀ \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="0ef81-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="0ef81-126">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="0ef81-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0ef81-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0ef81-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="0ef81-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ef81-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ef81-129">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="0ef81-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



