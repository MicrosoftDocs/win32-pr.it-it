---
description: Filtro renderer DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro renderer DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123504"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="1943c-103">Filtro renderer DirectSound</span><span class="sxs-lookup"><span data-stu-id="1943c-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="1943c-104">Questo filtro esegue il rendering dell'audio tramite DirectSound.</span><span class="sxs-lookup"><span data-stu-id="1943c-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="1943c-105">Questo filtro è attualmente il renderer audio predefinito per il suono della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="1943c-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="1943c-106">Oltre alle funzionalità di rendering audio di base, questo filtro può elaborare le chiamate all'API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="1943c-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="1943c-107">Usare i metodi [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) per impostare e recuperare la finestra che gestirà la riproduzione audio.</span><span class="sxs-lookup"><span data-stu-id="1943c-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="1943c-108">Il renderer audio DirectSound è il filtro di rendering audio predefinito per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1943c-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1943c-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="1943c-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1943c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="1943c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1943c-111">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="1943c-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1943c-112">Tipo principale: MEDIATYPE_AudioSubtypes:</span><span class="sxs-lookup"><span data-stu-id="1943c-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="1943c-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="1943c-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="1943c-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="1943c-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="1943c-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="1943c-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="1943c-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="1943c-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="1943c-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="1943c-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="1943c-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="1943c-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="1943c-119">Tipo formato: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="1943c-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1943c-120">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="1943c-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1943c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1943c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1943c-122">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="1943c-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1943c-123">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="1943c-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1943c-124">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="1943c-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1943c-125">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="1943c-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1943c-126">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="1943c-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="1943c-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="1943c-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1943c-128">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1943c-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1943c-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="1943c-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1943c-130">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="1943c-130">Executable</span></span></td>
<td><span data-ttu-id="1943c-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1943c-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1943c-132"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="1943c-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1943c-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="1943c-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1943c-134"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="1943c-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1943c-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="1943c-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1943c-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="1943c-136">Remarks</span></span>

<span data-ttu-id="1943c-137">Questo filtro funge da wrapper per un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="1943c-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="1943c-138">Per enumerare i dispositivi audio disponibili nel sistema dell'utente, usare l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoria renderer audio (CLSID \_ AudioRendererCategory).</span><span class="sxs-lookup"><span data-stu-id="1943c-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="1943c-139">Per ogni dispositivo audio, la categoria renderer audio contiene due istanze di filtro.</span><span class="sxs-lookup"><span data-stu-id="1943c-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="1943c-140">Uno di questi corrisponde al renderer DirectSound e l'altro corrisponde al filtro del [renderer audio (Wave out)](audio-renderer--waveout--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1943c-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="1943c-141">L'istanza di DirectSound ha il nome descrittivo "DirectSound: *DeviceName*", dove *DeviceName* è il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1943c-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="1943c-142">Il nome descrittivo dell'istanza di Wave out è *DeviceName*.</span><span class="sxs-lookup"><span data-stu-id="1943c-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="1943c-143">La categoria del renderer audio contiene due istanze di filtro aggiuntive, denominate "dispositivo DirectSound predefinito" e "dispositivo di onda predefinito".</span><span class="sxs-lookup"><span data-stu-id="1943c-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="1943c-144">Questi corrispondono al dispositivo audio predefinito, come scelto dall'utente tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="1943c-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="1943c-145">In realtà eseguono il mapping a una delle coppie descritte nel paragrafo precedente.</span><span class="sxs-lookup"><span data-stu-id="1943c-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="1943c-146">Ad esempio, se il sistema dispone di due dispositivi audio, il dispositivo A e il dispositivo B, la categoria di renderer audio conterrà quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1943c-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="1943c-147">Dispositivo A</span><span class="sxs-lookup"><span data-stu-id="1943c-147">Device A</span></span>
-   <span data-ttu-id="1943c-148">DirectSound: dispositivo A</span><span class="sxs-lookup"><span data-stu-id="1943c-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="1943c-149">Dispositivo B</span><span class="sxs-lookup"><span data-stu-id="1943c-149">Device B</span></span>
-   <span data-ttu-id="1943c-150">DirectSound: dispositivo B</span><span class="sxs-lookup"><span data-stu-id="1943c-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="1943c-151">Dispositivo DirectSound predefinito</span><span class="sxs-lookup"><span data-stu-id="1943c-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="1943c-152">Dispositivo di profrequenza predefinito</span><span class="sxs-lookup"><span data-stu-id="1943c-152">Default WaveOut Device</span></span>

<span data-ttu-id="1943c-153">Se l'utente ha selezionato il dispositivo come predefinito, "dispositivo DirectSound predefinito" equivale a "DirectSound: dispositivo A" e "dispositivo di onda predefinito" è equivalente a "dispositivo A".</span><span class="sxs-lookup"><span data-stu-id="1943c-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="1943c-154">Se l'utente seleziona il dispositivo B come dispositivo predefinito, questi mapping cambieranno.</span><span class="sxs-lookup"><span data-stu-id="1943c-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="1943c-155">Al "dispositivo DirectSound predefinito" viene assegnato un valore di Merit \_ preferenziale.</span><span class="sxs-lookup"><span data-stu-id="1943c-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="1943c-156">Gli altri hanno meriti di \_ merito \_ non \_ usare.</span><span class="sxs-lookup"><span data-stu-id="1943c-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="1943c-157">Pertanto, la connessione intelligente sceglierà sempre il dispositivo DirectSound predefinito.</span><span class="sxs-lookup"><span data-stu-id="1943c-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="1943c-158">Il filtro renderer DirectSound supporta il suono 3D attraverso le interfacce DirectSound **IDirectSound3DBuffer** e **IDirectSound3dListener** .</span><span class="sxs-lookup"><span data-stu-id="1943c-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="1943c-159">È anche possibile eseguire una query sul filtro per le versioni correnti di queste interfacce, **IDirectSound3DBuffer8** e **IDirectSound3dListener8**.</span><span class="sxs-lookup"><span data-stu-id="1943c-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="1943c-160">Eseguire il grafo prima di chiamare i metodi su queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="1943c-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1943c-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1943c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1943c-162">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="1943c-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




