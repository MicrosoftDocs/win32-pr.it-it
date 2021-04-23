---
description: Filtro AVI Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro AVI Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909469"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="8fba7-103">Filtro AVI Filter</span><span class="sxs-lookup"><span data-stu-id="8fba7-103">AVI Compressor Filter</span></span>

<span data-ttu-id="8fba7-104">Il filtro AVI Ntfs consente ai codec VCM (Video Compression Manager) di unirsi a un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="8fba7-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="8fba7-105">Ogni codec viene visualizzato come un'istanza separata del filtro.</span><span class="sxs-lookup"><span data-stu-id="8fba7-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="8fba7-106">Non è possibile creare direttamente questo filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="8fba7-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="8fba7-107">È invece necessario usare l'enumeratore del dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="8fba7-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="8fba7-108">Per altre informazioni, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="8fba7-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="8fba7-109">Il pin di input del filtro si connette ai filtri che generano dati video non compressi, ad esempio i filtri di acquisizione video o il filtro [AVI Splitter.](avi-splitter-filter.md)</span><span class="sxs-lookup"><span data-stu-id="8fba7-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="8fba7-110">Il pin di output del filtro si connette in genere a un filtro MUX, ad esempio il filtro [Mux AVI.](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="8fba7-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="8fba7-111">Se il codec supporta una finestra di dialogo di configurazione VFW o una finestra di dialogo Informazioni su, un'applicazione può visualizzarlo usando [**l'interfaccia IAMVfwCompressDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)</span><span class="sxs-lookup"><span data-stu-id="8fba7-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="8fba7-112">I file MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.</span><span class="sxs-lookup"><span data-stu-id="8fba7-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



| <span data-ttu-id="8fba7-113">Label</span><span class="sxs-lookup"><span data-stu-id="8fba7-113">Label</span></span> | <span data-ttu-id="8fba7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8fba7-114">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fba7-115">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="8fba7-115">Filter Interfaces</span></span>                        | <span data-ttu-id="8fba7-116">[**IAMVfwCompressDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="8fba7-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="8fba7-117">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="8fba7-117">Input Pin Media Types</span></span>                    | <span data-ttu-id="8fba7-118">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="8fba7-118">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="8fba7-119">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="8fba7-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8fba7-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8fba7-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="8fba7-121">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="8fba7-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="8fba7-122">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="8fba7-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="8fba7-123">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="8fba7-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8fba7-124">[**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8fba7-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8fba7-125">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="8fba7-125">Filter CLSID</span></span>                             | <span data-ttu-id="8fba7-126">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8fba7-126">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="8fba7-127">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8fba7-127">Property Page CLSID</span></span>                      | <span data-ttu-id="8fba7-128">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8fba7-128">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="8fba7-129">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="8fba7-129">Executable</span></span>                               | <span data-ttu-id="8fba7-130">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="8fba7-130">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8fba7-131">Merito</span><span class="sxs-lookup"><span data-stu-id="8fba7-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="8fba7-132">MERITO \_ NON \_ \_ USARE</span><span class="sxs-lookup"><span data-stu-id="8fba7-132">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="8fba7-133">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="8fba7-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8fba7-134">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="8fba7-134">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="8fba7-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fba7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fba7-136">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="8fba7-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



