---
description: Filtro decodificatore MPEG-1 audio
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro decodificatore MPEG-1 audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304217"
---
# <a name="mpeg-1-audio-decoder-filter"></a><span data-ttu-id="1d38b-103">Filtro decodificatore MPEG-1 audio</span><span class="sxs-lookup"><span data-stu-id="1d38b-103">MPEG-1 Audio Decoder Filter</span></span>

<span data-ttu-id="1d38b-104">Decodifica l'audio MPEG-1 Layer I e il livello II al PCM.</span><span class="sxs-lookup"><span data-stu-id="1d38b-104">Decodes MPEG-1 Layer I and Layer II audio to PCM.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d38b-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="1d38b-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1d38b-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="1d38b-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d38b-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="1d38b-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1d38b-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="1d38b-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span></span><br/> <span data-ttu-id="1d38b-109">I sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="1d38b-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="1d38b-110">MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="1d38b-110">MEDIASUBTYPE_MPEG1Packet</span></span></li>
<li><span data-ttu-id="1d38b-111">MEDIASUBTYPE_MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="1d38b-111">MEDIASUBTYPE_MPEG1Payload</span></span></li>
<li><span data-ttu-id="1d38b-112">MEDIASUBTYPE_MPEG1AudioPayload</span><span class="sxs-lookup"><span data-stu-id="1d38b-112">MEDIASUBTYPE_MPEG1AudioPayload</span></span></li>
<li><span data-ttu-id="1d38b-113">GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="1d38b-113">GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d38b-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="1d38b-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1d38b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d38b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d38b-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="1d38b-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1d38b-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="1d38b-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d38b-118">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="1d38b-118">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1d38b-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d38b-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d38b-120">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="1d38b-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="1d38b-121">CLSID_CMpegAudioCodec</span><span class="sxs-lookup"><span data-stu-id="1d38b-121">CLSID_CMpegAudioCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d38b-122">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1d38b-122">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1d38b-123">CLSID_MpegAudioDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="1d38b-123">CLSID_MpegAudioDecoderPropertyPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d38b-124">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="1d38b-124">Executable</span></span></td>
<td><span data-ttu-id="1d38b-125">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1d38b-125">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d38b-126"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="1d38b-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1d38b-127">0x03680001</span><span class="sxs-lookup"><span data-stu-id="1d38b-127">0x03680001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d38b-128"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="1d38b-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1d38b-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1d38b-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1d38b-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d38b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d38b-131">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="1d38b-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




