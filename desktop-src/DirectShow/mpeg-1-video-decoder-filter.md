---
description: Filtro decodificatore video MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro decodificatore video MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303851"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="9a5e6-103">Filtro decodificatore video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9a5e6-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="9a5e6-104">Decodifica il video MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9a5e6-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a5e6-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="9a5e6-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="9a5e6-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a5e6-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="9a5e6-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="9a5e6-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="9a5e6-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="9a5e6-109">I sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="9a5e6-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="9a5e6-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="9a5e6-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a5e6-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="9a5e6-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="9a5e6-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="9a5e6-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a5e6-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="9a5e6-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="9a5e6-115">Tipo principale: <strong>MEDIATYPE_Video</strong>,</span><span class="sxs-lookup"><span data-stu-id="9a5e6-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="9a5e6-116">Tipo di formato: <strong>FORMAT_VideoInfo</strong> o <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="9a5e6-117">Sottotipi</span><span class="sxs-lookup"><span data-stu-id="9a5e6-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="9a5e6-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="9a5e6-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="9a5e6-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="9a5e6-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="9a5e6-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="9a5e6-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="9a5e6-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="9a5e6-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a5e6-126">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="9a5e6-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="9a5e6-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="9a5e6-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a5e6-128">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="9a5e6-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="9a5e6-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a5e6-130">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9a5e6-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="9a5e6-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="9a5e6-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a5e6-132">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="9a5e6-132">Executable</span></span></td>
<td><span data-ttu-id="9a5e6-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="9a5e6-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a5e6-134"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="9a5e6-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="9a5e6-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="9a5e6-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a5e6-136"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="9a5e6-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="9a5e6-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="9a5e6-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9a5e6-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a5e6-138">Remarks</span></span>

<span data-ttu-id="9a5e6-139">Questo filtro può decodificare in una superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="9a5e6-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="9a5e6-140">Il filtro usa MMX se il computer supporta MMX.</span><span class="sxs-lookup"><span data-stu-id="9a5e6-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a5e6-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a5e6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5e6-142">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="9a5e6-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




