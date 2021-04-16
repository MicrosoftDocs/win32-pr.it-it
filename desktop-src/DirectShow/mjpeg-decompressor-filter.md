---
description: Filtro di decompressione MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro di decompressione MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522457"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="4c446-103">Filtro di decompressione MJPEG</span><span class="sxs-lookup"><span data-stu-id="4c446-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="4c446-104">Questo filtro decodifica un flusso video da JPEG di movimento a video non compresso.</span><span class="sxs-lookup"><span data-stu-id="4c446-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="4c446-105">Alcune fotocamere digitali video producono un flusso video JPEG di movimento.</span><span class="sxs-lookup"><span data-stu-id="4c446-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c446-106">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="4c446-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="4c446-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4c446-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="4c446-108">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="4c446-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="4c446-109">\_Video di MEDIATYPE, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="4c446-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="4c446-110">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="4c446-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="4c446-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="4c446-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="4c446-112">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="4c446-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="4c446-113">MEDIATYPE \_ video, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="4c446-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="4c446-114">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="4c446-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="4c446-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="4c446-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="4c446-116">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="4c446-116">Filter CLSID</span></span>                             | <span data-ttu-id="4c446-117">\_MJPEGDEC CLSID</span><span class="sxs-lookup"><span data-stu-id="4c446-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="4c446-118">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="4c446-118">Property Page CLSID</span></span>                      | <span data-ttu-id="4c446-119">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="4c446-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="4c446-120">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="4c446-120">Executable</span></span>                               | <span data-ttu-id="4c446-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="4c446-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="4c446-122">Merito</span><span class="sxs-lookup"><span data-stu-id="4c446-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="4c446-123">VALORE \_ normale</span><span class="sxs-lookup"><span data-stu-id="4c446-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="4c446-124">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="4c446-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4c446-125">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="4c446-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="4c446-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c446-126">Remarks</span></span>

<span data-ttu-id="4c446-127">Questo filtro è compatibile con il video Motion JPEG che usa il codice FOURCC ' MJPG '.</span><span class="sxs-lookup"><span data-stu-id="4c446-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="4c446-128">Non può decodificare altre varianti del JPEG di movimento.</span><span class="sxs-lookup"><span data-stu-id="4c446-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="4c446-129">Per questi, è necessario usare un filtro per il decodificatore di terze parti.</span><span class="sxs-lookup"><span data-stu-id="4c446-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c446-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c446-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c446-131">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="4c446-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



