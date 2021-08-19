---
description: Filtro decodificatore audio MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro decodificatore audio MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0324cf9626ad73192bd403581f5933907f014ce93e6f23a05fa1bd155863e009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153017"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Filtro decodificatore audio MPEG-1

Decodifica l'audio MPEG-1 Layer I e Layer II in PCM.



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
<td>MEDIATYPE_Audio, FORMAT_WaveFormatEx<br/> Sono validi i sottotipi seguenti:<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1Packet</li>
<li>MEDIASUBTYPE_MPEG1Payload</li>
<li>MEDIASUBTYPE_MPEG1AudioPayload</li>
<li>Guid_null</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM</td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtro CLSID</td>
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

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




