---
description: Filtro del convertitore dello spazio colori
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtro del convertitore dello spazio colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481181"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="1b166-103">Filtro del convertitore dello spazio colori</span><span class="sxs-lookup"><span data-stu-id="1b166-103">Color Space Converter Filter</span></span>

<span data-ttu-id="1b166-104">Questo filtro di trasformazione viene convertito da un tipo di colore RGB a un altro tipo RGB, ad esempio tra colore RGB a 24 bit e a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="1b166-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="1b166-105">Poiché questo tipo di conversione viene in genere gestito in modo più efficiente all'interno di un decompressore video, l'uso principale del convertitore dello spazio colori è quando l'origine del flusso è costituita da frame RGB non compressi.</span><span class="sxs-lookup"><span data-stu-id="1b166-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b166-106">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="1b166-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1b166-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b166-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b166-108">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="1b166-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1b166-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="1b166-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="1b166-110">I sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="1b166-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="1b166-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="1b166-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="1b166-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="1b166-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="1b166-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="1b166-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="1b166-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="1b166-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="1b166-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="1b166-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b166-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="1b166-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1b166-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b166-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b166-118">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="1b166-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1b166-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="1b166-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="1b166-120">I sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="1b166-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="1b166-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="1b166-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="1b166-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="1b166-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="1b166-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="1b166-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="1b166-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="1b166-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="1b166-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="1b166-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b166-126">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="1b166-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1b166-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b166-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b166-128">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="1b166-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="1b166-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="1b166-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b166-130">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1b166-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1b166-131">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1b166-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b166-132">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="1b166-132">Executable</span></span></td>
<td><span data-ttu-id="1b166-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1b166-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b166-134"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="1b166-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1b166-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="1b166-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b166-136"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="1b166-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1b166-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1b166-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1b166-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b166-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b166-139">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b166-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




