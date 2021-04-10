---
description: Gestione della qualità dei video
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Gestione della qualità dei video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966977"
---
# <a name="video-quality-management"></a><span data-ttu-id="d7367-103">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="d7367-103">Video Quality Management</span></span>

<span data-ttu-id="d7367-104">Questo argomento descrive alcuni miglioramenti apportati alla pipeline video in Windows 7, sia per Microsoft Media Foundation che per Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d7367-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="d7367-105">In un mondo perfetto, i video non dovrebbero mai essere glitch, indipendentemente dalla risoluzione video o dal carico CPU/GPU.</span><span class="sxs-lookup"><span data-stu-id="d7367-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="d7367-106">In realtà, ovviamente, la pipeline video deve essere in grado di gestire le risorse hardware finite ed è necessario in modo adattivo la riproduzione adatta all'ambiente di sistema.</span><span class="sxs-lookup"><span data-stu-id="d7367-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="d7367-107">Gli obiettivi per la gestione della qualità dei video sono:</span><span class="sxs-lookup"><span data-stu-id="d7367-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="d7367-108">Ridurre le anomalie (riquadri rilasciati o tardivi).</span><span class="sxs-lookup"><span data-stu-id="d7367-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="d7367-109">Ridurre l'utilizzo della memoria, soprattutto nella GPU.</span><span class="sxs-lookup"><span data-stu-id="d7367-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="d7367-110">Ridurre il consumo di energia, soprattutto nei computer portatili con alimentazione a batteria.</span><span class="sxs-lookup"><span data-stu-id="d7367-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="d7367-111">Ottenere la migliore qualità di immagine possibile, dati vincoli di risorse.</span><span class="sxs-lookup"><span data-stu-id="d7367-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="d7367-112">Mantieni il video sincronizzato con audio.</span><span class="sxs-lookup"><span data-stu-id="d7367-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="d7367-113">Alcuni di questi obiettivi sono contrari, soprattutto nei sistemi di fascia bassa.</span><span class="sxs-lookup"><span data-stu-id="d7367-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="d7367-114">Generalmente esiste un compromesso tra velocità e qualità.</span><span class="sxs-lookup"><span data-stu-id="d7367-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="d7367-115">La glitching è più discutibile rispetto alle riduzioni moderate nella qualità visiva.</span><span class="sxs-lookup"><span data-stu-id="d7367-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="d7367-116">L'importanza relativa del consumo di energia elettrica varia a seconda dell'ambiente. in un computer portatile alimentato da batteria, è molto importante.</span><span class="sxs-lookup"><span data-stu-id="d7367-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="d7367-117">In Windows 7, il renderer video avanzato (EVR) offre un supporto migliore per la gestione della qualità dei video.</span><span class="sxs-lookup"><span data-stu-id="d7367-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="d7367-118">Sia la pipeline Media Foundation che la pipeline DirectShow sono state aggiornate per sfruttare i vantaggi di queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d7367-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="d7367-119">Viene utilizzato un approccio A due punte:</span><span class="sxs-lookup"><span data-stu-id="d7367-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="d7367-120">Prima dell'avvio della riproduzione, la pipeline può eseguire ottimizzazioni statiche, in base alle impostazioni di risparmio energia dell'utente e alle informazioni sull'hardware.</span><span class="sxs-lookup"><span data-stu-id="d7367-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="d7367-121">Una volta avviata la riproduzione, la pipeline può applicare ottimizzazioni dinamiche in base alle prestazioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d7367-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="d7367-122">Gestione della qualità in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7367-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="d7367-123">Per abilitare le ottimizzazioni statiche, impostare l'attributo di [ \_ \_ \_ \_ ottimizzazione della riproduzione statica della topologia MF](mf-topology-static-playback-optimizations.md) sulla topologia parziale prima di risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="d7367-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="d7367-124">Il caricatore della topologia esegue una query su questo attributo nel metodo [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="d7367-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="d7367-125">Se si abilitano le ottimizzazioni statiche, è necessario impostare altri due attributi nella topologia:</span><span class="sxs-lookup"><span data-stu-id="d7367-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="d7367-126">Attributo</span><span class="sxs-lookup"><span data-stu-id="d7367-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="d7367-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7367-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d7367-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF \_ \_ massima riproduzione topologia \_ \_ Dim</span><span class="sxs-lookup"><span data-stu-id="d7367-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="d7367-129">Specifica la dimensione massima della finestra di riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="d7367-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="d7367-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_framerate di riproduzione della topologia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="d7367-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="d7367-131">Specifica la frequenza di aggiornamento del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d7367-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="d7367-132">Questi due attributi consentono alla pipeline di calcolare l'impostazione più efficace per la gestione della qualità.</span><span class="sxs-lookup"><span data-stu-id="d7367-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="d7367-133">Le ottimizzazioni dinamiche vengono eseguite dal gestore qualità.</span><span class="sxs-lookup"><span data-stu-id="d7367-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="d7367-134">Non è necessario eseguire alcuna operazione per abilitare il gestore qualità; viene abilitata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d7367-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="d7367-135">Il responsabile qualità era presente in Windows Vista; in Windows 7, EVR è in grado di rispondere meglio ai messaggi provenienti dal gestore qualità.</span><span class="sxs-lookup"><span data-stu-id="d7367-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="d7367-136">Gestione della qualità in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7367-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="d7367-137">DirectShow supporta le ottimizzazioni statiche e dinamiche per la riproduzione di DVD.</span><span class="sxs-lookup"><span data-stu-id="d7367-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="d7367-138">Per abilitare queste ottimizzazioni in un'applicazione di riproduzione DVD, impostare i flag seguenti nel parametro *dwFlags* del metodo **IDvdGraphBuilder:: RenderDvdVideoVolume** :</span><span class="sxs-lookup"><span data-stu-id="d7367-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="d7367-139">Flag</span><span class="sxs-lookup"><span data-stu-id="d7367-139">Flag</span></span>                  | <span data-ttu-id="d7367-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7367-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="d7367-141">\_grafico am DVD \_ ADAPT \_</span><span class="sxs-lookup"><span data-stu-id="d7367-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="d7367-142">Abilita le ottimizzazioni statiche.</span><span class="sxs-lookup"><span data-stu-id="d7367-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="d7367-143">\_QoS DVD \_ EVR \_</span><span class="sxs-lookup"><span data-stu-id="d7367-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="d7367-144">Abilita le ottimizzazioni dinamiche.</span><span class="sxs-lookup"><span data-stu-id="d7367-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="d7367-145">Altre applicazioni DirectShow possono abilitare le ottimizzazioni dinamiche chiamando il metodo [**IEVRFilterConfigEx:: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) direttamente sul filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="d7367-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="d7367-146">Specificare il **flag \_ EnableQoS di EVRFilterConfigPrefs** .</span><span class="sxs-lookup"><span data-stu-id="d7367-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="d7367-147">Le ottimizzazioni statiche in DirectShow sono limitate alla riproduzione di DVD.</span><span class="sxs-lookup"><span data-stu-id="d7367-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="d7367-148">Gestione della qualità in EVR</span><span class="sxs-lookup"><span data-stu-id="d7367-148">Quality Management in the EVR</span></span>

<span data-ttu-id="d7367-149">EVR supporta alcuni nuovi flag di configurazione per la gestione della qualità.</span><span class="sxs-lookup"><span data-stu-id="d7367-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="d7367-150">Se si abilitano le ottimizzazioni di gestione della qualità descritte in precedenza, non è necessario impostare direttamente questi flag.</span><span class="sxs-lookup"><span data-stu-id="d7367-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="d7367-151">Tuttavia, sono documentati per le applicazioni che vogliono un controllo più granulare sui EVR.</span><span class="sxs-lookup"><span data-stu-id="d7367-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="d7367-152">Impostare i flag seguenti nel mixer EVR chiamando il metodo [**IMFVideoMixerControl2:: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :</span><span class="sxs-lookup"><span data-stu-id="d7367-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7367-153">Flags</span><span class="sxs-lookup"><span data-stu-id="d7367-153">Flags</span></span></th>
<th><span data-ttu-id="d7367-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7367-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d7367-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="d7367-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="d7367-157">Ignora il secondo campo di ogni frame interlacciato.</span><span class="sxs-lookup"><span data-stu-id="d7367-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="d7367-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="d7367-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="d7367-160">Usare il deinterlacciamento Bob, anche se il driver supporta una modalità di deinterlacciamento di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="d7367-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d7367-161">Impostare i flag seguenti nel relatore EVR chiamando il metodo [**IMFVideoDisplayControl:: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :</span><span class="sxs-lookup"><span data-stu-id="d7367-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7367-162">Flags</span><span class="sxs-lookup"><span data-stu-id="d7367-162">Flags</span></span></th>
<th><span data-ttu-id="d7367-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7367-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d7367-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="d7367-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="d7367-166">Limitazione dell'output per la corrispondenza della larghezza di banda della GPU.</span><span class="sxs-lookup"><span data-stu-id="d7367-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="d7367-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="d7367-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="d7367-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="d7367-169">Chiamate di batch Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d7367-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="d7367-170">Questa ottimizzazione consente al sistema di immettere gli stati inattivi con maggiore frequenza, riducendo così il consumo di energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="d7367-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d7367-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="d7367-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="d7367-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="d7367-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="d7367-173">Eseguire la combinazione di video usando un rettangolo inferiore al rettangolo di output.</span><span class="sxs-lookup"><span data-stu-id="d7367-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="d7367-174">Ridimensionare il risultato alla dimensione di output corretta.</span><span class="sxs-lookup"><span data-stu-id="d7367-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d7367-175">Inoltre, il sink multimediale EVR supporta gli attributi di configurazione che corrispondono a ognuno di questi flag:</span><span class="sxs-lookup"><span data-stu-id="d7367-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="d7367-176">\_AllowBatching EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="d7367-177">\_AllowDropToBob EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="d7367-178">\_AllowDropToHalfInterlace EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="d7367-179">\_AllowScaling EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="d7367-180">\_AllowDropToThrottle EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="d7367-181">\_ForceBatching EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="d7367-182">\_ForceBob EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="d7367-183">\_ForceHalfInterlace EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="d7367-184">\_ForceScaling EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="d7367-185">\_ForceThrottle EVRConfig</span><span class="sxs-lookup"><span data-stu-id="d7367-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="d7367-186">Prima dell'avvio della riproduzione, è possibile impostare questi attributi direttamente nel sink di supporto EVR, come alternativa alla chiamata dei metodi [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) e [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="d7367-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="d7367-187">Per impostare questi attributi, eseguire una query sul sink multimediale EVR per [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="d7367-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7367-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7367-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7367-189">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="d7367-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




