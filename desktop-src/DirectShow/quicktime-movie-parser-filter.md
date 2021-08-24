---
description: Filtro del parser di film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro del parser di film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e5d82b7e0f4da1365c7dcdf753463cb3c846e5fae82a839de0c21a5800bc5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747441"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro del parser di film QuickTime

Questo componente è stato rimosso da Windows Vista e sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

Il filtro QuickTime Movie Parser suddivide i ® QuickTime® Apple in flussi audio e video. Supporta QuickTime 2.0 e versioni precedenti. Il pin di input si connette a un filtro di origine, ad esempio il filtro [Origine file](file-source--async--filter.md) asincrona o il filtro Origine [file URL.](file-source--url--filter.md) Il parser usa il [filtro AVI Decompressor](avi-decompressor-filter.md) o [QT Decompressor](qt-decompressor-filter.md) per decomprimere i file QuickTime. Il filtro crea un pin di output per il flusso video e un pin di output per il flusso audio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td><ul>
<li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li>
<li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID del filtro</td>
<td>CLSID_QuickTimeParser</td>
</tr>
<tr class="odd">
<td>CLSID pagina delle proprietà</td>
<td>Nessuna pagina delle proprietà.</td>
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



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



