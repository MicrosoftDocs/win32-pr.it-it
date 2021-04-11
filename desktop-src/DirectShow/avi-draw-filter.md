---
description: Filtro di disegni AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro di disegni AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123681"
---
# <a name="avi-draw-filter"></a><span data-ttu-id="c882e-103">Filtro di disegni AVI</span><span class="sxs-lookup"><span data-stu-id="c882e-103">AVI Draw Filter</span></span>

<span data-ttu-id="c882e-104">Il filtro di disegno AVI viene inserito automaticamente in un grafico di riproduzione invece che nel [decompressore AVI](avi-decompressor-filter.md) quando il video viene restituito a un monitor di TV NTSC esterno.</span><span class="sxs-lookup"><span data-stu-id="c882e-104">The AVI Draw filter is pulled automatically into a playback graph instead of the [AVI Decompressor](avi-decompressor-filter.md) when video is being output to an external NTSC television monitor.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c882e-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="c882e-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="c882e-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="c882e-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c882e-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="c882e-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="c882e-108">Tipo principale: MEDIATYPE_VideoSubtypes:</span><span class="sxs-lookup"><span data-stu-id="c882e-108">Major Type: MEDIATYPE_VideoSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="c882e-109">MEDIASUBTYPE_MJPG</span><span class="sxs-lookup"><span data-stu-id="c882e-109">MEDIASUBTYPE_MJPG</span></span></li>
<li><span data-ttu-id="c882e-110">MEDIASUBTYPE_TVMJ</span><span class="sxs-lookup"><span data-stu-id="c882e-110">MEDIASUBTYPE_TVMJ</span></span></li>
<li><span data-ttu-id="c882e-111">MEDIASUBTYPE_WAKE</span><span class="sxs-lookup"><span data-stu-id="c882e-111">MEDIASUBTYPE_WAKE</span></span></li>
<li><span data-ttu-id="c882e-112">MEDIASUBTYPE_CFCC</span><span class="sxs-lookup"><span data-stu-id="c882e-112">MEDIASUBTYPE_CFCC</span></span></li>
<li><span data-ttu-id="c882e-113">MEDIASUBTYPE_IJPG</span><span class="sxs-lookup"><span data-stu-id="c882e-113">MEDIASUBTYPE_IJPG</span></span></li>
<li><span data-ttu-id="c882e-114">MEDIASUBTYPE_Plum</span><span class="sxs-lookup"><span data-stu-id="c882e-114">MEDIASUBTYPE_Plum</span></span></li>
<li><span data-ttu-id="c882e-115">MEDIASUBTYPE_DVCS</span><span class="sxs-lookup"><span data-stu-id="c882e-115">MEDIASUBTYPE_DVCS</span></span></li>
<li><span data-ttu-id="c882e-116">MEDIASUBTYPE_DVSD</span><span class="sxs-lookup"><span data-stu-id="c882e-116">MEDIASUBTYPE_DVSD</span></span></li>
<li><span data-ttu-id="c882e-117">MEDIASUBTYPE_MDVF</span><span class="sxs-lookup"><span data-stu-id="c882e-117">MEDIASUBTYPE_MDVF</span></span></li>
<li><span data-ttu-id="c882e-118">Tipo formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="c882e-118">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c882e-119">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="c882e-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="c882e-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c882e-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c882e-121">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="c882e-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="c882e-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="c882e-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c882e-123">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="c882e-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="c882e-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c882e-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c882e-125">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="c882e-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="c882e-126">CLSID_AVIDraw</span><span class="sxs-lookup"><span data-stu-id="c882e-126">CLSID_AVIDraw</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c882e-127">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c882e-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="c882e-128">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c882e-128">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c882e-129">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="c882e-129">Executable</span></span></td>
<td><span data-ttu-id="c882e-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c882e-130">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c882e-131"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="c882e-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="c882e-132">MERIT_NORMAL + 100</span><span class="sxs-lookup"><span data-stu-id="c882e-132">MERIT_NORMAL + 100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c882e-133"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="c882e-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="c882e-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c882e-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c882e-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c882e-135">Remarks</span></span>

<span data-ttu-id="c882e-136">Poiché il filtro di disegno AVI e il [filtro di acquisizione VFW](vfw-capture-filter.md) si connettono entrambi allo stesso hardware, non possono trovarsi nello stesso grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c882e-136">Since the AVI Draw filter and the [VFW Capture Filter](vfw-capture-filter.md) both connect to the same hardware, they cannot be in the same filter graph.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c882e-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c882e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c882e-138">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="c882e-138">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




