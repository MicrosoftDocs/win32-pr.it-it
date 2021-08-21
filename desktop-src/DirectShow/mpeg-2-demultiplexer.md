---
description: Questo filtro demultiplexa i flussi di trasporto e programma MPEG-2 recapitati in modalità push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2 Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4648a456e8f7fa43274486111973fa2255ab29e4e674bc249e1c2a3c64a7b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152984"
---
# <a name="mpeg-2-demultiplexer"></a>MPEG-2 Demultiplexer

Questo filtro demultiplexa i flussi di trasporto e programma MPEG-2 recapitati in modalità push. A partire Windows XP, questo filtro supporta anche i flussi di programma in modalità pull (riproduzione di file). Nelle piattaforme precedenti usare il filtro [mpeg-2 splitter](mpeg-2-splitter.md) per i flussi del programma in modalità pull. Questo filtro può essere usato in qualsiasi tipo di grafico di filtro, incluso un grafico di filtro tv digitale BDA.

> [!Note]  
> Il demultiplexer MPEG-2 non supporta la ricerca accurata dei frame.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td>Tutte le modalità:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Filtro IBaseFilter</strong></a></li>
<li><strong>ISpecifyPropertyPages</strong></li>
</ul>
Solo modalità push:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_STREAM<br/> Sottotipo:<br/>
<ul>
<li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li>
</ul>
Per altre informazioni, vedere <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>I flussi elementari audio e video devono avere un tipo principale di MEDIATYPE_Audio o MEDIATYPE_Video.<br/> Per altre informazioni, vedere <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a>solo modalità push <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl:</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource,</strong></a> <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br/> Solo modalità pull: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br/></td>
</tr>
<tr class="even">
<td>CLSID del filtro</td>
<td>CLSID_MPEG2Demultiplexer</td>
</tr>
<tr class="odd">
<td>CLSID pagina delle proprietà</td>
<td>Disponibile solo per i test. Usare <strong>l'interfaccia ISpecifyPropertyPages</strong> per accedere alle pagine delle proprietà</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>mpg2splt.ax</td>
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

Per l'output di flussi elementari audio e video, il demux deve ricevere i flussi PCR e SCR. Sul lato input, ciò significa che un flusso di trasporto deve contenere le tabelle PAT e PMT che definiscono il PID per il flusso PCR. e i flussi di programma devono contenere almeno un'intestazione di tipo pack.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |
| Fine del supporto server<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Uso del demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




