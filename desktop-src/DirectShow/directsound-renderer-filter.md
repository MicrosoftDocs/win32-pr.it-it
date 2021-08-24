---
description: Filtro renderer DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro renderer DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e754c81ba9ac6d22141735ac1488218461d9ea63ef81f7bb947cb3e72fd81d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966321"
---
# <a name="directsound-renderer-filter"></a>Filtro renderer DirectSound

Questo filtro esegue il rendering dell'audio usando DirectSound. Questo filtro è attualmente il renderer audio predefinito per l'audio waveform.

Oltre alle funzionalità di rendering del suono di base, questo filtro può elaborare le chiamate all'API DirectSound. Usare i [**metodi IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) per impostare e recuperare la finestra che gestirà la riproduzione audio. Il renderer audio DirectSound è il filtro di rendering audio predefinito per DirectShow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockListener,</strong></a> <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio,</strong></a> <strong>IDirectSound3DBuffer,</strong> <strong>IDirectSound3dListener,</strong> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_AudioSubtypes:<br/>
<ul>
<li>MEDIASUBTYPE_PCM</li>
<li>MEDIASUBTYPE_IEEE_FLOAT</li>
<li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li>
<li>MEDIASUBTYPE_RAW_SPORT</li>
<li>MEDIASUBTYPE_SPDIF_TAG_241h</li>
<li>MEDIASUBTYPE_DRM_Audio</li>
</ul>
Tipo di formato: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Non applicabile.</td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td>Non applicabile.</td>
</tr>
<tr class="even">
<td>CLSID del filtro</td>
<td>CLSID_DSoundRender</td>
</tr>
<tr class="odd">
<td>CLSID pagina delle proprietà</td>
<td>CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_PREFERRED</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_AudioRendererCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Questo filtro funge da wrapper per un dispositivo audio. Per enumerare i dispositivi audio disponibili nel sistema dell'utente, usare l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoria del renderer audio (CLSID \_ AudioRendererCategory). Per ogni dispositivo audio, la categoria renderer audio contiene due istanze di filtro. Uno di questi corrisponde al renderer DirectSound e l'altro corrisponde al filtro [Audio Renderer (WaveOut).](audio-renderer--waveout--filter.md) L'istanza di DirectSound ha il nome descrittivo "DirectSound: *DeviceName",* dove *DeviceName* è il nome del dispositivo. L'istanza WaveOut ha il nome *descrittivo DeviceName*.

La categoria del renderer audio contiene due istanze di filtro aggiuntive, denominate "Dispositivo DirectSound predefinito" e "Dispositivo WaveOut predefinito". Corrispondono al dispositivo audio predefinito, scelto dall'utente tramite il Pannello di controllo. In realtà, vengono mappati a una delle coppie descritte nel paragrafo precedente. Ad esempio, se il sistema ha due dispositivi audio, Dispositivo A e Dispositivo B, la categoria del renderer audio conterrà quanto segue:

-   Dispositivo A
-   DirectSound: dispositivo A
-   Dispositivo B
-   DirectSound: Dispositivo B
-   Dispositivo DirectSound predefinito
-   Dispositivo WaveOut predefinito

Se l'utente ha selezionato Il dispositivo A come dispositivo predefinito, "Dispositivo DirectSound predefinito" equivale a "DirectSound: Dispositivo A" e "Dispositivo WaveOut predefinito" equivale a "Dispositivo A". Se l'utente seleziona Il dispositivo B come dispositivo predefinito, questi mapping cambieranno.

A "Default DirectSound Device" (Dispositivo DirectSound predefinito) viene assegnato un equivalente di PREFERRED \_ PREFERRED. Gli altri hanno il merito DI NON \_ \_ \_ USARE. Di conseguenza, Connessione intelligente sceglierà sempre il dispositivo DirectSound predefinito.

Il filtro renderer DirectSound supporta l'audio 3D tramite le interfacce **DirectSound IDirectSound3DBuffer** e **IDirectSound3dListener.** È anche possibile eseguire una query sul filtro per le versioni correnti di queste interfacce, **IDirectSound3DBuffer8** **e IDirectSound3dListener8.** Eseguire il grafo prima di chiamare metodi su queste interfacce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




