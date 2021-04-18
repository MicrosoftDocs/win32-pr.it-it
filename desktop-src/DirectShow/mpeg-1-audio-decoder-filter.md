---
description: Filtro decodificatore MPEG-1 audio
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro decodificatore MPEG-1 audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304217"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Filtro decodificatore MPEG-1 audio

Decodifica l'audio MPEG-1 Layer I e il livello II al PCM.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>MEDIATYPE_Audio, FORMAT_WaveFormatEx<br/> I sottotipi seguenti sono validi:<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1Packet</li>
<li>MEDIASUBTYPE_MPEG1Payload</li>
<li>MEDIASUBTYPE_MPEG1AudioPayload</li>
<li>GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_CMpegAudioCodec</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>CLSID_MpegAudioDecoderPropertyPage</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>0x03680001</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




