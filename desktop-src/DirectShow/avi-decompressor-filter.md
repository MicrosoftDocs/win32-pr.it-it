---
description: Filtro Decompressore AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro Decompressore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746922"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="f85b8-103">Filtro Decompressore AVI</span><span class="sxs-lookup"><span data-stu-id="f85b8-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="f85b8-104">Il filtro del decompressore AVI consente ai codec di Gestione compressione video di aggiungere un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="f85b8-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="f85b8-105">Non è necessario che l'applicazione aggiunga il filtro al grafico di filtro; Quando necessario, viene eseguito il pull automatico dal gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f85b8-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="f85b8-106">Quando il gestore del grafo del filtro compila un grafico per eseguire il rendering di un file AVI, verifica FOURCC nell'intestazione AVI del file per determinare se il flusso video è compresso.</span><span class="sxs-lookup"><span data-stu-id="f85b8-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="f85b8-107">In tal caso, il gestore del grafico di filtro aggiunge il decompressore AVI, che quindi Cerca nel registro di sistema un decompressore installato in grado di gestire il file.</span><span class="sxs-lookup"><span data-stu-id="f85b8-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="f85b8-108">I decompressori MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.</span><span class="sxs-lookup"><span data-stu-id="f85b8-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="f85b8-109">Sul suo pin upstream, il decompressore AVI si connette in genere al [separatore AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f85b8-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="f85b8-110">Sul pin di output si connette in genere al [renderer video](video-renderer-filter.md) o al [filtro Mux AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f85b8-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85b8-111">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="f85b8-111">Filter Interfaces</span></span>                        | [<span data-ttu-id="f85b8-112">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="f85b8-112">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="f85b8-113">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="f85b8-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="f85b8-114">Tipo principale: MEDIATYPE \_ VideoSubtype: deve corrispondere al codice FourCC per il tipo di compressione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-114">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="f85b8-115">Per altre informazioni, vedere [codici FourCC](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f85b8-115">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="f85b8-116">Tipo di formato: FORMAT \_ videoinfo</span><span class="sxs-lookup"><span data-stu-id="f85b8-116">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="f85b8-117">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="f85b8-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f85b8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f85b8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="f85b8-119">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="f85b8-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="f85b8-120">MEDIATYPE \_ video, MEDIASUBTYPE \_ null, Format \_ videoinfo</span><span class="sxs-lookup"><span data-stu-id="f85b8-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="f85b8-121">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="f85b8-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f85b8-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f85b8-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="f85b8-123">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="f85b8-123">Filter CLSID</span></span>                             | <span data-ttu-id="f85b8-124">\_AVIDEC CLSID</span><span class="sxs-lookup"><span data-stu-id="f85b8-124">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="f85b8-125">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f85b8-125">Property Page CLSID</span></span>                      | <span data-ttu-id="f85b8-126">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f85b8-126">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="f85b8-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="f85b8-127">Executable</span></span>                               | <span data-ttu-id="f85b8-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f85b8-128">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="f85b8-129">Merito</span><span class="sxs-lookup"><span data-stu-id="f85b8-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="f85b8-130">VALORE \_ normale</span><span class="sxs-lookup"><span data-stu-id="f85b8-130">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="f85b8-131">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="f85b8-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f85b8-132">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="f85b8-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="f85b8-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f85b8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f85b8-134">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="f85b8-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




