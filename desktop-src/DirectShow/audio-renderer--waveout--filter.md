---
description: Filtro del renderer audio (Wave out)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro del renderer audio (Wave out)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304254"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="99d76-103">Filtro del renderer audio (Wave out)</span><span class="sxs-lookup"><span data-stu-id="99d76-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="99d76-104">Questo filtro usa l' \* API di Wave per eseguire il rendering dell'audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="99d76-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="99d76-105">Tuttavia, il [filtro renderer DirectSound](directsound-renderer-filter.md) fornisce la stessa funzionalità utilizzando DirectSound.</span><span class="sxs-lookup"><span data-stu-id="99d76-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="99d76-106">Per impostazione predefinita, Filter Graph Manager usa il renderer DirectSound anziché questo filtro.</span><span class="sxs-lookup"><span data-stu-id="99d76-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="99d76-107">La combinazione audio è disabilitata nel renderer audio di Wave, quindi se è necessario combinare più flussi audio durante la riproduzione, usare il renderer DirectSound.</span><span class="sxs-lookup"><span data-stu-id="99d76-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="99d76-108">Questo filtro non controlla il sottotipo del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="99d76-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="99d76-109">La struttura [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passata nel formato contiene le informazioni necessarie per la connessione.</span><span class="sxs-lookup"><span data-stu-id="99d76-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="99d76-110">Questo filtro supporta un intervallo di frequenze di campionamento che dipende dal driver audio.</span><span class="sxs-lookup"><span data-stu-id="99d76-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99d76-111">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="99d76-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="99d76-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="99d76-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="99d76-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="99d76-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="99d76-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="99d76-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="99d76-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="99d76-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="99d76-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="99d76-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="99d76-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="99d76-121">IPersistStream</span></span></li>
<li><span data-ttu-id="99d76-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="99d76-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99d76-124">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="99d76-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="99d76-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="99d76-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99d76-126">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="99d76-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="99d76-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="99d76-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="99d76-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="99d76-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99d76-130">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="99d76-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="99d76-131">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="99d76-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99d76-132">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="99d76-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="99d76-133">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="99d76-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99d76-134">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="99d76-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="99d76-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="99d76-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99d76-136">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="99d76-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="99d76-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="99d76-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99d76-138">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="99d76-138">Executable</span></span></td>
<td><span data-ttu-id="99d76-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="99d76-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99d76-140"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="99d76-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="99d76-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="99d76-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99d76-142"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="99d76-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="99d76-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="99d76-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="99d76-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99d76-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d76-145">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="99d76-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
