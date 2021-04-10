---
description: Filtro del separatore di flusso MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro del separatore di flusso MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125220"
---
# <a name="mpeg-1-stream-splitter-filter"></a>Filtro del separatore di flusso MPEG-1

Questo filtro suddivide un flusso di sistema MPEG-1 nei flussi audio e video dei componenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_Stream<br/> Sottotipi<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1System</li>
<li>MEDIASUBTYPE_MPEG1VideoCD</li>
<li>MEDIASUBTYPE_Audio</li>
<li>MEDIASUBTYPE_Video</li>
</ul>
Vedere <a href="mpeg-1-media-types.md"> <strong>tipi di supporto MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Tipo principale: MEDIATYPE_Audio o MEDIATYPE_Video<br/> Sottotipo: MEDIASUBTYPE_MPEG1Payload o MEDIASUBTYPE_MPEG1Packet<br/> Vedere <a href="mpeg-1-media-types.md"> <strong>tipi di supporto MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_MPEG1Splitter</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Nessuna pagina delle proprietà</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Questo file supporta solo la modalità pull tramite [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; non supporta la modalità push.

Poiché il contenuto MPEG-1 non è indicizzato, la ricerca può essere molto approssimativa. È in genere ideale per un flusso di sistema MPEG-1 a bitrate fisso, che in genere è hardware generato per il CD video.

Il filtro supporta l'interfaccia [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) per il recupero dei metadati ID3.

Non tutti i campioni MPEG hanno timestamp. La mancanza di un timestamp di un esempio MPEG non è un errore. Per gli sviluppatori di filtri, ciò significa che non è necessario restituire un codice di errore dal metodo **Receive** del PIN di input se [**IMediaSample:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) ha esito negativo. Se **Receive** restituisce un valore diverso da S \_ OK, la barra di divisione interrompe l'invio degli esempi.

Se il file contiene un flusso video, la barra di divisione MPEG-1 Stream supporta la ricerca in base al numero di frame. Per abilitare la ricerca basata su frame, chiamare [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in [Filter Graph Manager](filter-graph-manager.md) con il valore **\_ format time format \_ frame**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




