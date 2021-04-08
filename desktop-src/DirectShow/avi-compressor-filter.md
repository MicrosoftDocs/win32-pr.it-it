---
description: Filtro compressore AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro compressore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875946"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="302e8-103">Filtro compressore AVI</span><span class="sxs-lookup"><span data-stu-id="302e8-103">AVI Compressor Filter</span></span>

<span data-ttu-id="302e8-104">Il filtro del compressore AVI consente ai codec di Gestione compressione video di aggiungere un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="302e8-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="302e8-105">Ogni codec viene visualizzato come un'istanza separata del filtro.</span><span class="sxs-lookup"><span data-stu-id="302e8-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="302e8-106">Non è possibile creare direttamente questo filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="302e8-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="302e8-107">È invece necessario utilizzare l'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="302e8-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="302e8-108">Per ulteriori informazioni, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="302e8-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="302e8-109">Il pin di input del filtro si connette ai filtri che restituiscono dati video non compressi, ad esempio i filtri di acquisizione video o il [filtro separatore AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="302e8-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="302e8-110">Il pin di output del filtro in genere si connette a un filtro MUX, ad esempio il [filtro Mux AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="302e8-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="302e8-111">Se il codec supporta una finestra di dialogo di configurazione VFW obsoleta o una finestra di dialogo informazioni su, un'applicazione può visualizzarla usando l'interfaccia [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="302e8-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="302e8-112">I compressatori MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.</span><span class="sxs-lookup"><span data-stu-id="302e8-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="302e8-113">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="302e8-113">Filter Interfaces</span></span>                        | <span data-ttu-id="302e8-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="302e8-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="302e8-115">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="302e8-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="302e8-116">MEDIATYPE \_ video, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="302e8-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="302e8-117">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="302e8-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="302e8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="302e8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="302e8-119">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="302e8-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="302e8-120">MEDIATYPE \_ video, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="302e8-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="302e8-121">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="302e8-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="302e8-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="302e8-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="302e8-123">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="302e8-123">Filter CLSID</span></span>                             | <span data-ttu-id="302e8-124">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="302e8-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="302e8-125">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="302e8-125">Property Page CLSID</span></span>                      | <span data-ttu-id="302e8-126">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="302e8-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="302e8-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="302e8-127">Executable</span></span>                               | <span data-ttu-id="302e8-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="302e8-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="302e8-129">Merito</span><span class="sxs-lookup"><span data-stu-id="302e8-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="302e8-130">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="302e8-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="302e8-131">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="302e8-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="302e8-132">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="302e8-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="302e8-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="302e8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="302e8-134">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="302e8-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



