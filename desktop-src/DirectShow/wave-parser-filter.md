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
# <a name="wave-parser-filter"></a>Filtro del parser WAVE

Il filtro del parser WAVE analizza i dati audio in formato WAV da file WAV, au o AIF. Il filtro upstream deve essere il filtro origine [file](file-source--async--filter.md) asincrono, il filtro [origine file URL](file-source--url--filter.md) o un filtro di origine asincrono di terze parti compatibile contenente dati audio WAV. Il flusso di output è costituito da dati audio, che è possibile connettere direttamente a un filtro di rendering audio o a un filtro di trasformazione audio corrispondente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_StreamThe sottotipi seguenti sono validi:<br/>
<ul>
<li>MEDIASUBTYPE_AIFF</li>
<li>MEDIASUBTYPE_AU</li>
<li>MEDIASUBTYPE_WAVE</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Tipo principale: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM o un altro tipo di compressione. Vedere <a href="audio-subtypes.md"><strong>sottotipi audio</strong></a>.<br/> Tipo formato: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>{D51BD5A1-7548-11cf-A520-0080C77EF58A}</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Nessuna pagina delle proprietà.</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Questo filtro supporta i tipi di file seguenti:

-   WAVE (WAV)
-   AIFF e AIFF-C (. AIF)
-   AU (. au)

Tuttavia, presenta le seguenti limitazioni relative al formato audio:

-   L'audio deve essere PCM lineare a 8 bit o a 16 bit.
-   Per i file AIFF-C, l'audio deve essere decompresso, in ordine di byte big-endian (tipo di compressione ' NONE ').

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




