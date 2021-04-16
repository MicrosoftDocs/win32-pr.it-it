---
description: Filtro del decompressore QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro del decompressore QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481476"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="7a395-103">Filtro del decompressore QT</span><span class="sxs-lookup"><span data-stu-id="7a395-103">QT Decompressor Filter</span></span>

<span data-ttu-id="7a395-104">Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="7a395-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="7a395-105">È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a395-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="7a395-106">Il filtro del decompressore QT decomprime il video Apple® QuickTime® 2,0.</span><span class="sxs-lookup"><span data-stu-id="7a395-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="7a395-107">Questo formato viene in genere usato nei file QuickTime precedenti.</span><span class="sxs-lookup"><span data-stu-id="7a395-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a395-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="7a395-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7a395-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a395-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a395-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="7a395-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="7a395-111">MEDIATYPE_Video, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="7a395-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="7a395-112">I sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="7a395-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="7a395-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="7a395-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="7a395-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="7a395-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="7a395-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="7a395-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="7a395-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="7a395-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a395-117">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="7a395-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7a395-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a395-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a395-119">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="7a395-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7a395-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="7a395-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a395-121">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="7a395-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7a395-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a395-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a395-123">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="7a395-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="7a395-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="7a395-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a395-125">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="7a395-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7a395-126">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7a395-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a395-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="7a395-127">Executable</span></span></td>
<td><span data-ttu-id="7a395-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7a395-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a395-129"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="7a395-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7a395-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="7a395-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a395-131"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="7a395-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7a395-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7a395-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7a395-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a395-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a395-134">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a395-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




