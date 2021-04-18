---
description: Filtro wrapper ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro wrapper ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304271"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="395dd-103">Filtro wrapper ACM</span><span class="sxs-lookup"><span data-stu-id="395dd-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="395dd-104">Il filtro del wrapper ACM consente ai codec ACM (Audio Compression Manager) di aggiungere un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="395dd-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="395dd-105">Può fungere da filtro di decompressione o come filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="395dd-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="395dd-106">Come filtro di decompressione, il wrapper ACM viene visualizzato nella categoria "filtri DirectShow" (CLSID \_ LegacyAmFilterCategory) e ha un merito del \_ normale merito.</span><span class="sxs-lookup"><span data-stu-id="395dd-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="395dd-107">Il tipo di supporto di connessione al pin di input determina il codec utilizzato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="395dd-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="395dd-108">In genere, l'applicazione non deve aggiungere il filtro al grafico di filtro; Quando necessario, viene eseguito il pull automatico dal gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="395dd-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="395dd-109">La decompressione è solo l'audio PCM.</span><span class="sxs-lookup"><span data-stu-id="395dd-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="395dd-110">Come filtro di compressione, il wrapper ACM viene visualizzato nella categoria "comprimer audio" (CLSID \_ AudioCompressorCategory) ed è caratterizzato da un \_ merito \_ non \_ utilizzato.</span><span class="sxs-lookup"><span data-stu-id="395dd-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="395dd-111">Ogni codec viene visualizzato come un'istanza separata.</span><span class="sxs-lookup"><span data-stu-id="395dd-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="395dd-112">Per la compressione non è possibile creare direttamente il filtro con CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="395dd-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="395dd-113">È invece necessario utilizzare l'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="395dd-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="395dd-114">Per ulteriori informazioni, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="395dd-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="395dd-115">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="395dd-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="395dd-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="395dd-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="395dd-117">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="395dd-117">Input pin media types</span></span></td>
<td><span data-ttu-id="395dd-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="395dd-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="395dd-119">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="395dd-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="395dd-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="395dd-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="395dd-121">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="395dd-121">Output pin media types</span></span></td>
<td><span data-ttu-id="395dd-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx. qualsiasi combinazione dei seguenti elementi è possibile:</span><span class="sxs-lookup"><span data-stu-id="395dd-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="395dd-123">Campioni al secondo (kHz): 44,1, 22,05, 11,025 o 8,0.</span><span class="sxs-lookup"><span data-stu-id="395dd-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="395dd-124">Canali: stereo o mono.</span><span class="sxs-lookup"><span data-stu-id="395dd-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="395dd-125">BITS per campione: 8 o 16.</span><span class="sxs-lookup"><span data-stu-id="395dd-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="395dd-126">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="395dd-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="395dd-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="395dd-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="395dd-128">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="395dd-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="395dd-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="395dd-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="395dd-130">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="395dd-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="395dd-131">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="395dd-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="395dd-132">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="395dd-132">Executable</span></span></td>
<td><span data-ttu-id="395dd-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="395dd-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="395dd-134"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="395dd-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="395dd-135">MERIT_NORMAL o MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="395dd-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="395dd-136"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="395dd-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="395dd-137">CLSID_LegacyAmFilterCategory o CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="395dd-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="395dd-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="395dd-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="395dd-139">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="395dd-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




