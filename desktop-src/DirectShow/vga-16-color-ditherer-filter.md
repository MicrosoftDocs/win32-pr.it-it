---
description: Filtro del sequelo di colore VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro del sequelo di colore VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057827"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="2da48-103">Filtro del sequelo di colore VGA 16</span><span class="sxs-lookup"><span data-stu-id="2da48-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="2da48-104">Il filtro di tipo VGA a 16 colori viene convertito da un tipo di colore RGB a una visualizzazione a colori a 4 bit, in modo che i flussi video AVI e MPEG possano essere visualizzati nei monitoraggi a 16 colori precedenti.</span><span class="sxs-lookup"><span data-stu-id="2da48-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="2da48-105">Questo filtro viene inserito nel grafico tra un filtro decompressore e un filtro renderer video.</span><span class="sxs-lookup"><span data-stu-id="2da48-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da48-106">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="2da48-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="2da48-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="2da48-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="2da48-108">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="2da48-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="2da48-109">\_Video di MEDIATYPE, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="2da48-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="2da48-110">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="2da48-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="2da48-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2da48-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="2da48-112">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="2da48-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="2da48-113">\_Video di MEDIATYPE, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="2da48-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="2da48-114">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="2da48-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="2da48-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2da48-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="2da48-116">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="2da48-116">Filter CLSID</span></span>                             | <span data-ttu-id="2da48-117">\_Dithering CLSID</span><span class="sxs-lookup"><span data-stu-id="2da48-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="2da48-118">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="2da48-118">Property Page CLSID</span></span>                      | <span data-ttu-id="2da48-119">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="2da48-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="2da48-120">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="2da48-120">Executable</span></span>                               | <span data-ttu-id="2da48-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2da48-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="2da48-122">Merito</span><span class="sxs-lookup"><span data-stu-id="2da48-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="2da48-123">VALORE \_ improbabile</span><span class="sxs-lookup"><span data-stu-id="2da48-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="2da48-124">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="2da48-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2da48-125">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="2da48-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="2da48-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2da48-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da48-127">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="2da48-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



