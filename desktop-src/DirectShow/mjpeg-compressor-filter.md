---
description: Filtro MJPEG Filter
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro MJPEG Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910009"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="3a8bc-103">Filtro MJPEG Filter</span><span class="sxs-lookup"><span data-stu-id="3a8bc-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="3a8bc-104">Questo filtro comprime un flusso video non compresso, usando la compressione JPEG del movimento.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="3a8bc-105">Label</span><span class="sxs-lookup"><span data-stu-id="3a8bc-105">Label</span></span> | <span data-ttu-id="3a8bc-106">Valore</span><span class="sxs-lookup"><span data-stu-id="3a8bc-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8bc-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="3a8bc-107">Filter Interfaces</span></span>                        | <span data-ttu-id="3a8bc-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="3a8bc-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="3a8bc-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="3a8bc-110">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="3a8bc-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="3a8bc-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="3a8bc-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="3a8bc-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3a8bc-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="3a8bc-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="3a8bc-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="3a8bc-114">MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="3a8bc-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="3a8bc-115">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="3a8bc-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="3a8bc-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3a8bc-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3a8bc-117">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="3a8bc-117">Filter CLSID</span></span>                             | <span data-ttu-id="3a8bc-118">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="3a8bc-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="3a8bc-119">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="3a8bc-119">Property Page CLSID</span></span>                      | <span data-ttu-id="3a8bc-120">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="3a8bc-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="3a8bc-121">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="3a8bc-121">Executable</span></span>                               | <span data-ttu-id="3a8bc-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3a8bc-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3a8bc-123">Merito</span><span class="sxs-lookup"><span data-stu-id="3a8bc-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="3a8bc-124">MERITO \_ NON \_ \_ USARE</span><span class="sxs-lookup"><span data-stu-id="3a8bc-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="3a8bc-125">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="3a8bc-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3a8bc-126">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="3a8bc-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="3a8bc-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a8bc-127">Remarks</span></span>

<span data-ttu-id="3a8bc-128">Questo filtro codifica usando il sottotipo multimediale MEDIASUBTYPE MJPG, che corrisponde al codice \_ FOURCC 'MJPG'.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a8bc-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a8bc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a8bc-130">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="3a8bc-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



