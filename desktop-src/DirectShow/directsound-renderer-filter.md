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
# <a name="directsound-renderer-filter"></a>Filtro renderer DirectSound

Questo filtro esegue il rendering dell'audio tramite DirectSound. Questo filtro è attualmente il renderer audio predefinito per il suono della forma d'onda.

Oltre alle funzionalità di rendering audio di base, questo filtro può elaborare le chiamate all'API DirectSound. Usare i metodi [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) per impostare e recuperare la finestra che gestirà la riproduzione audio. Il renderer audio DirectSound è il filtro di rendering audio predefinito per DirectShow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
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
Tipo formato: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Non applicabile.</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td>Non applicabile.</td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_DSoundRender</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
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

Questo filtro funge da wrapper per un dispositivo audio. Per enumerare i dispositivi audio disponibili nel sistema dell'utente, usare l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoria renderer audio (CLSID \_ AudioRendererCategory). Per ogni dispositivo audio, la categoria renderer audio contiene due istanze di filtro. Uno di questi corrisponde al renderer DirectSound e l'altro corrisponde al filtro del [renderer audio (Wave out)](audio-renderer--waveout--filter.md) . L'istanza di DirectSound ha il nome descrittivo "DirectSound: *DeviceName*", dove *DeviceName* è il nome del dispositivo. Il nome descrittivo dell'istanza di Wave out è *DeviceName*.

La categoria del renderer audio contiene due istanze di filtro aggiuntive, denominate "dispositivo DirectSound predefinito" e "dispositivo di onda predefinito". Questi corrispondono al dispositivo audio predefinito, come scelto dall'utente tramite il pannello di controllo. In realtà eseguono il mapping a una delle coppie descritte nel paragrafo precedente. Ad esempio, se il sistema dispone di due dispositivi audio, il dispositivo A e il dispositivo B, la categoria di renderer audio conterrà quanto segue:

-   Dispositivo A
-   DirectSound: dispositivo A
-   Dispositivo B
-   DirectSound: dispositivo B
-   Dispositivo DirectSound predefinito
-   Dispositivo di profrequenza predefinito

Se l'utente ha selezionato il dispositivo come predefinito, "dispositivo DirectSound predefinito" equivale a "DirectSound: dispositivo A" e "dispositivo di onda predefinito" è equivalente a "dispositivo A". Se l'utente seleziona il dispositivo B come dispositivo predefinito, questi mapping cambieranno.

Al "dispositivo DirectSound predefinito" viene assegnato un valore di Merit \_ preferenziale. Gli altri hanno meriti di \_ merito \_ non \_ usare. Pertanto, la connessione intelligente sceglierà sempre il dispositivo DirectSound predefinito.

Il filtro renderer DirectSound supporta il suono 3D attraverso le interfacce DirectSound **IDirectSound3DBuffer** e **IDirectSound3dListener** . È anche possibile eseguire una query sul filtro per le versioni correnti di queste interfacce, **IDirectSound3DBuffer8** e **IDirectSound3dListener8**. Eseguire il grafo prima di chiamare i metodi su queste interfacce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




