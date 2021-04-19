---
description: Filtro del parser WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro del parser WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319538"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="f147f-103">Filtro del parser WAVE</span><span class="sxs-lookup"><span data-stu-id="f147f-103">WAVE Parser Filter</span></span>

<span data-ttu-id="f147f-104">Il filtro del parser WAVE analizza i dati audio in formato WAV da file WAV, au o AIF.</span><span class="sxs-lookup"><span data-stu-id="f147f-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="f147f-105">Il filtro upstream deve essere il filtro origine [file](file-source--async--filter.md) asincrono, il filtro [origine file URL](file-source--url--filter.md) o un filtro di origine asincrono di terze parti compatibile contenente dati audio WAV.</span><span class="sxs-lookup"><span data-stu-id="f147f-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="f147f-106">Il flusso di output è costituito da dati audio, che è possibile connettere direttamente a un filtro di rendering audio o a un filtro di trasformazione audio corrispondente.</span><span class="sxs-lookup"><span data-stu-id="f147f-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f147f-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="f147f-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f147f-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span><span class="sxs-lookup"><span data-stu-id="f147f-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f147f-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="f147f-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="f147f-110">Tipo principale: MEDIATYPE_StreamThe sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="f147f-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="f147f-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="f147f-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="f147f-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="f147f-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="f147f-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="f147f-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f147f-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="f147f-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f147f-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f147f-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f147f-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="f147f-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f147f-117">Tipo principale: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM o un altro tipo di compressione.</span><span class="sxs-lookup"><span data-stu-id="f147f-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="f147f-118">Vedere <a href="audio-subtypes.md"><strong>sottotipi audio</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f147f-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="f147f-119">Tipo formato: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="f147f-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f147f-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="f147f-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f147f-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="f147f-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f147f-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="f147f-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="f147f-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="f147f-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f147f-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f147f-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f147f-125">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f147f-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f147f-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="f147f-126">Executable</span></span></td>
<td><span data-ttu-id="f147f-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f147f-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f147f-128"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="f147f-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f147f-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="f147f-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f147f-130"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="f147f-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f147f-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f147f-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f147f-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f147f-132">Remarks</span></span>

<span data-ttu-id="f147f-133">Questo filtro supporta i tipi di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="f147f-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="f147f-134">WAVE (WAV)</span><span class="sxs-lookup"><span data-stu-id="f147f-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="f147f-135">AIFF e AIFF-C (. AIF)</span><span class="sxs-lookup"><span data-stu-id="f147f-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="f147f-136">AU (. au)</span><span class="sxs-lookup"><span data-stu-id="f147f-136">AU (.au)</span></span>

<span data-ttu-id="f147f-137">Tuttavia, presenta le seguenti limitazioni relative al formato audio:</span><span class="sxs-lookup"><span data-stu-id="f147f-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="f147f-138">L'audio deve essere PCM lineare a 8 bit o a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="f147f-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="f147f-139">Per i file AIFF-C, l'audio deve essere decompresso, in ordine di byte big-endian (tipo di compressione ' NONE ').</span><span class="sxs-lookup"><span data-stu-id="f147f-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="f147f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f147f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f147f-141">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="f147f-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




