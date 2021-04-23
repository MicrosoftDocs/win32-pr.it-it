---
description: Filtro decompressore MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro decompressore MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910019"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="fb540-103">Filtro decompressore MJPEG</span><span class="sxs-lookup"><span data-stu-id="fb540-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="fb540-104">Questo filtro decodifica un flusso video da MOTION JPEG a un video non compresso.</span><span class="sxs-lookup"><span data-stu-id="fb540-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="fb540-105">Alcune videocamere digitali producono un flusso video JPEG in movimento.</span><span class="sxs-lookup"><span data-stu-id="fb540-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="fb540-106">Label</span><span class="sxs-lookup"><span data-stu-id="fb540-106">Label</span></span> | <span data-ttu-id="fb540-107">Valore</span><span class="sxs-lookup"><span data-stu-id="fb540-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb540-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="fb540-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="fb540-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="fb540-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="fb540-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="fb540-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="fb540-111">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="fb540-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="fb540-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="fb540-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="fb540-113">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="fb540-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="fb540-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="fb540-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="fb540-115">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="fb540-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="fb540-116">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="fb540-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="fb540-117">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="fb540-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="fb540-118">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="fb540-118">Filter CLSID</span></span>                             | <span data-ttu-id="fb540-119">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="fb540-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="fb540-120">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="fb540-120">Property Page CLSID</span></span>                      | <span data-ttu-id="fb540-121">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="fb540-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="fb540-122">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="fb540-122">Executable</span></span>                               | <span data-ttu-id="fb540-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="fb540-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="fb540-124">Merito</span><span class="sxs-lookup"><span data-stu-id="fb540-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="fb540-125">MERIT \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="fb540-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="fb540-126">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="fb540-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="fb540-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="fb540-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="fb540-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb540-128">Remarks</span></span>

<span data-ttu-id="fb540-129">Questo filtro è compatibile con il video JPEG di movimento che usa il codice FOURCC 'MJPG'.</span><span class="sxs-lookup"><span data-stu-id="fb540-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="fb540-130">Non può decodificare altri tipi di movimento JPEG.</span><span class="sxs-lookup"><span data-stu-id="fb540-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="fb540-131">Per queste operazioni, è necessario usare un filtro decodificatore di terze parti.</span><span class="sxs-lookup"><span data-stu-id="fb540-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb540-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb540-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb540-133">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="fb540-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



