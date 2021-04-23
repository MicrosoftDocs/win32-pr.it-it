---
description: Filtro decompressore AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro decompressore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910099"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="19721-103">Filtro decompressore AVI</span><span class="sxs-lookup"><span data-stu-id="19721-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="19721-104">Il filtro AVI Decompressor consente ai codec VCM (Video Compression Manager) di unire un grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="19721-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="19721-105">L'applicazione non deve aggiungere il filtro al grafico dei filtri. viene estratto automaticamente da Filter Graph Manager quando necessario.</span><span class="sxs-lookup"><span data-stu-id="19721-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="19721-106">Quando Filter Graph Manager compila un grafo per eseguire il rendering di un file AVI, controlla FOURCC nell'intestazione AVI del file per determinare se il flusso video è compresso.</span><span class="sxs-lookup"><span data-stu-id="19721-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="19721-107">In caso contrario, Filter Graph Manager aggiunge il decompressore AVI, che cerca nel Registro di sistema un decompressore installato in grado di gestire il file.</span><span class="sxs-lookup"><span data-stu-id="19721-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="19721-108">I decompressori MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.</span><span class="sxs-lookup"><span data-stu-id="19721-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="19721-109">Sul pin upstream il decompressore AVI si connette in genere alla barra di divisione [AVI.](avi-splitter-filter.md)</span><span class="sxs-lookup"><span data-stu-id="19721-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="19721-110">Nel pin di output si connette in genere al [renderer video o](video-renderer-filter.md) al filtro [Mux AVI.](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="19721-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



| <span data-ttu-id="19721-111">Label</span><span class="sxs-lookup"><span data-stu-id="19721-111">Label</span></span> | <span data-ttu-id="19721-112">Valore</span><span class="sxs-lookup"><span data-stu-id="19721-112">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19721-113">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="19721-113">Filter Interfaces</span></span>                        | [<span data-ttu-id="19721-114">**Filtro IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="19721-114">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="19721-115">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="19721-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="19721-116">Tipo principale: MEDIATYPE \_ VideoSubtype: deve corrispondere al codice FOURCC per il tipo di compressione.</span><span class="sxs-lookup"><span data-stu-id="19721-116">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="19721-117">Per altre informazioni, vedere [FOURCC Codes](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="19721-117">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="19721-118">Tipo di formato: FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="19721-118">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="19721-119">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="19721-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="19721-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="19721-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="19721-121">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="19721-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="19721-122">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="19721-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="19721-123">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="19721-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="19721-124">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="19721-124">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="19721-125">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="19721-125">Filter CLSID</span></span>                             | <span data-ttu-id="19721-126">CLSID \_ AVIDec</span><span class="sxs-lookup"><span data-stu-id="19721-126">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="19721-127">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="19721-127">Property Page CLSID</span></span>                      | <span data-ttu-id="19721-128">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="19721-128">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="19721-129">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="19721-129">Executable</span></span>                               | <span data-ttu-id="19721-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="19721-130">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="19721-131">Merito</span><span class="sxs-lookup"><span data-stu-id="19721-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="19721-132">MERITO \_ NORMALE</span><span class="sxs-lookup"><span data-stu-id="19721-132">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="19721-133">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="19721-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="19721-134">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="19721-134">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="19721-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19721-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19721-136">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="19721-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




