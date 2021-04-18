---
description: Filtro compressione MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro compressione MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304220"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="22f97-103">Filtro compressione MJPEG</span><span class="sxs-lookup"><span data-stu-id="22f97-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="22f97-104">Questo filtro comprime un flusso video non compresso, usando la compressione JPEG di movimento.</span><span class="sxs-lookup"><span data-stu-id="22f97-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22f97-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="22f97-105">Filter Interfaces</span></span>                        | <span data-ttu-id="22f97-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="22f97-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="22f97-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="22f97-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="22f97-108">MEDIATYPE \_ video, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="22f97-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="22f97-109">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="22f97-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="22f97-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="22f97-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="22f97-111">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="22f97-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="22f97-112">\_Video di MEDIATYPE, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="22f97-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="22f97-113">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="22f97-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="22f97-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="22f97-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="22f97-115">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="22f97-115">Filter CLSID</span></span>                             | <span data-ttu-id="22f97-116">\_MJPGENC CLSID</span><span class="sxs-lookup"><span data-stu-id="22f97-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="22f97-117">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="22f97-117">Property Page CLSID</span></span>                      | <span data-ttu-id="22f97-118">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="22f97-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="22f97-119">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="22f97-119">Executable</span></span>                               | <span data-ttu-id="22f97-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="22f97-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="22f97-121">Merito</span><span class="sxs-lookup"><span data-stu-id="22f97-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="22f97-122">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="22f97-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="22f97-123">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="22f97-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="22f97-124">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="22f97-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="22f97-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="22f97-125">Remarks</span></span>

<span data-ttu-id="22f97-126">Questo filtro codifica usando il sottotipo di supporto MEDIASUBTYPE \_ MJPG, che corrisponde al codice FourCC ' MJPG '.</span><span class="sxs-lookup"><span data-stu-id="22f97-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22f97-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22f97-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22f97-128">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="22f97-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



