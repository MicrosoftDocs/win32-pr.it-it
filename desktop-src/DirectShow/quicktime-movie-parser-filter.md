---
description: Filtro del parser film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro del parser film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341951"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="07641-103">Filtro del parser film QuickTime</span><span class="sxs-lookup"><span data-stu-id="07641-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="07641-104">Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="07641-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="07641-105">È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="07641-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="07641-106">Il filtro QuickTime Movie Parser divide Apple® QuickTime® i dati nei flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="07641-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="07641-107">Supporta QuickTime 2,0 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="07641-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="07641-108">Il pin di input si connette a un filtro di origine, ad esempio il filtro origine [file asincrono](file-source--async--filter.md) o il filtro [origine file URL](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="07641-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="07641-109">Il parser usa il filtro Decompressore [AVI](avi-decompressor-filter.md) o decompressore [QT](qt-decompressor-filter.md) per decomprimere i file QuickTime.</span><span class="sxs-lookup"><span data-stu-id="07641-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="07641-110">Il filtro crea un pin di output per il flusso video e un pin di output per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="07641-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07641-111">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="07641-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="07641-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="07641-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07641-113">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="07641-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="07641-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span><span class="sxs-lookup"><span data-stu-id="07641-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07641-115">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="07641-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="07641-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="07641-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07641-117">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="07641-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="07641-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="07641-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="07641-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="07641-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07641-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="07641-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="07641-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="07641-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07641-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="07641-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="07641-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="07641-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07641-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="07641-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="07641-125">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="07641-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07641-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="07641-126">Executable</span></span></td>
<td><span data-ttu-id="07641-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="07641-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07641-128"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="07641-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="07641-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="07641-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07641-130"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="07641-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="07641-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="07641-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="07641-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07641-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07641-133">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="07641-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



