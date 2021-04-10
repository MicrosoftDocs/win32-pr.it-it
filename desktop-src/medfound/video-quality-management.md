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
# <a name="video-quality-management"></a>Gestione della qualità dei video

Questo argomento descrive alcuni miglioramenti apportati alla pipeline video in Windows 7, sia per Microsoft Media Foundation che per Microsoft DirectShow.

In un mondo perfetto, i video non dovrebbero mai essere glitch, indipendentemente dalla risoluzione video o dal carico CPU/GPU. In realtà, ovviamente, la pipeline video deve essere in grado di gestire le risorse hardware finite ed è necessario in modo adattivo la riproduzione adatta all'ambiente di sistema. Gli obiettivi per la gestione della qualità dei video sono:

-   Ridurre le anomalie (riquadri rilasciati o tardivi).
-   Ridurre l'utilizzo della memoria, soprattutto nella GPU.
-   Ridurre il consumo di energia, soprattutto nei computer portatili con alimentazione a batteria.
-   Ottenere la migliore qualità di immagine possibile, dati vincoli di risorse.
-   Mantieni il video sincronizzato con audio.

Alcuni di questi obiettivi sono contrari, soprattutto nei sistemi di fascia bassa. Generalmente esiste un compromesso tra velocità e qualità. La glitching è più discutibile rispetto alle riduzioni moderate nella qualità visiva. L'importanza relativa del consumo di energia elettrica varia a seconda dell'ambiente. in un computer portatile alimentato da batteria, è molto importante.

In Windows 7, il renderer video avanzato (EVR) offre un supporto migliore per la gestione della qualità dei video. Sia la pipeline Media Foundation che la pipeline DirectShow sono state aggiornate per sfruttare i vantaggi di queste funzionalità. Viene utilizzato un approccio A due punte:

-   Prima dell'avvio della riproduzione, la pipeline può eseguire ottimizzazioni statiche, in base alle impostazioni di risparmio energia dell'utente e alle informazioni sull'hardware.
-   Una volta avviata la riproduzione, la pipeline può applicare ottimizzazioni dinamiche in base alle prestazioni in fase di esecuzione.

## <a name="quality-management-in-media-foundation"></a>Gestione della qualità in Media Foundation

Per abilitare le ottimizzazioni statiche, impostare l'attributo di [ \_ \_ \_ \_ ottimizzazione della riproduzione statica della topologia MF](mf-topology-static-playback-optimizations.md) sulla topologia parziale prima di risolvere la topologia. Il caricatore della topologia esegue una query su questo attributo nel metodo [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Se si abilitano le ottimizzazioni statiche, è necessario impostare altri due attributi nella topologia:



| Attributo                                                                                                                                      | Descrizione                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF \_ \_ massima riproduzione topologia \_ \_ Dim<br/>   | Specifica la dimensione massima della finestra di riproduzione video.<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_framerate di riproduzione della topologia MF \_ \_<br/> | Specifica la frequenza di aggiornamento del monitoraggio.<br/>                      |



 

Questi due attributi consentono alla pipeline di calcolare l'impostazione più efficace per la gestione della qualità.

Le ottimizzazioni dinamiche vengono eseguite dal gestore qualità. Non è necessario eseguire alcuna operazione per abilitare il gestore qualità; viene abilitata automaticamente. Il responsabile qualità era presente in Windows Vista; in Windows 7, EVR è in grado di rispondere meglio ai messaggi provenienti dal gestore qualità.

## <a name="quality-management-in-directshow"></a>Gestione della qualità in DirectShow

DirectShow supporta le ottimizzazioni statiche e dinamiche per la riproduzione di DVD. Per abilitare queste ottimizzazioni in un'applicazione di riproduzione DVD, impostare i flag seguenti nel parametro *dwFlags* del metodo **IDvdGraphBuilder:: RenderDvdVideoVolume** :



| Flag                  | Descrizione                    |
|-----------------------|--------------------------------|
| \_grafico am DVD \_ ADAPT \_ | Abilita le ottimizzazioni statiche.  |
| \_QoS DVD \_ EVR \_     | Abilita le ottimizzazioni dinamiche. |



 

Altre applicazioni DirectShow possono abilitare le ottimizzazioni dinamiche chiamando il metodo [**IEVRFilterConfigEx:: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) direttamente sul filtro EVR. Specificare il **flag \_ EnableQoS di EVRFilterConfigPrefs** .

> [!Note]  
> Le ottimizzazioni statiche in DirectShow sono limitate alla riproduzione di DVD.

 

## <a name="quality-management-in-the-evr"></a>Gestione della qualità in EVR

EVR supporta alcuni nuovi flag di configurazione per la gestione della qualità. Se si abilitano le ottimizzazioni di gestione della qualità descritte in precedenza, non è necessario impostare direttamente questi flag. Tuttavia, sono documentati per le applicazioni che vogliono un controllo più granulare sui EVR.

Impostare i flag seguenti nel mixer EVR chiamando il metodo [**IMFVideoMixerControl2:: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li>
<li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li>
</ul></td>
<td>Ignora il secondo campo di ogni frame interlacciato.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li>
<li><strong>MFVideoMixPrefs_ForceBob</strong></li>
</ul></td>
<td>Usare il deinterlacciamento Bob, anche se il driver supporta una modalità di deinterlacciamento di qualità superiore.</td>
</tr>
</tbody>
</table>



 

Impostare i flag seguenti nel relatore EVR chiamando il metodo [**IMFVideoDisplayControl:: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li>
<li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li>
</ul></td>
<td>Limitazione dell'output per la corrispondenza della larghezza di banda della GPU.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceBatching</strong></li>
<li><strong>MFVideoRenderPrefs_AllowBatching</strong></li>
</ul></td>
<td>Chiamate di batch Direct3D. Questa ottimizzazione consente al sistema di immettere gli stati inattivi con maggiore frequenza, riducendo così il consumo di energia elettrica.</td>
</tr>
<tr class="odd">
<td><ul>
<li>MFVideoRenderPrefs_ForceScaling</li>
<li>MFVideoRenderPrefs_AllowScaling</li>
</ul></td>
<td>Eseguire la combinazione di video usando un rettangolo inferiore al rettangolo di output. Ridimensionare il risultato alla dimensione di output corretta.</td>
</tr>
</tbody>
</table>



 

Inoltre, il sink multimediale EVR supporta gli attributi di configurazione che corrispondono a ognuno di questi flag:

-   [\_AllowBatching EVRConfig](evrconfig-allowbatching.md)
-   [\_AllowDropToBob EVRConfig](evrconfig-allowdroptobob.md)
-   [\_AllowDropToHalfInterlace EVRConfig](evrconfig-allowdroptohalfinterlace.md)
-   [\_AllowScaling EVRConfig](evrconfig-allowscaling.md)
-   [\_AllowDropToThrottle EVRConfig](evrconfig-allowdroptothrottle.md)
-   [\_ForceBatching EVRConfig](evrconfig-forcebatching.md)
-   [\_ForceBob EVRConfig](evrconfig-forcebob.md)
-   [\_ForceHalfInterlace EVRConfig](evrconfig-forcehalfinterlace.md)
-   [\_ForceScaling EVRConfig](evrconfig-forcescaling.md)
-   [\_ForceThrottle EVRConfig](evrconfig-forcethrottle.md)

Prima dell'avvio della riproduzione, è possibile impostare questi attributi direttamente nel sink di supporto EVR, come alternativa alla chiamata dei metodi [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) e [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . Per impostare questi attributi, eseguire una query sul sink multimediale EVR per [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 




