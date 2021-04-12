---
description: Splitter MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Splitter MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225453"
---
# <a name="mpeg-2-splitter"></a>Splitter MPEG-2

A partire da Microsoft® Windows® XP, il filtro della barra di divisione MPEG-2 è deprecato. Usare invece [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) .

Nelle piattaforme precedenti usare il separatore MPEG-2 per i flussi di programma MPEG-2 recapitati in modalità pull che contengono almeno uno dei tipi di flusso seguenti: MPEG-2 video; Audio MPEG-2; Audio AC3 codificato come definito per il video DVD; o audio PCM codificato come definito per il video DVD. Questo filtro analizza i flussi, crea un pin di output per ogni flusso e genera i pacchetti audio o video MPEG compressi in un filtro di decodificatore MPEG-2.

Per i flussi di programma e trasporto distribuiti in modalità push, usare il [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md)su tutte le piattaforme.

> [!Note]  
> Il separatore MPEG-2 non supporta la ricerca con precisione dei frame.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td><ul>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Dipende dal tipo di flusso. Vedere <a href="mpeg-2-splitter-media-types.md">tipi di supporti Splitter MPEG-2</a></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Uso della barra di divisione MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



