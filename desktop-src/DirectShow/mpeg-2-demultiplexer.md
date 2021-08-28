---
description: Questo filtro demultiplexa i flussi di trasporto e programma MPEG-2 recapitati in modalità push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2 Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21898cb4fa3c16b07508dc3370c519d3edfbced
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983954"
---
# <a name="mpeg-2-demultiplexer"></a>MPEG-2 Demultiplexer

Questo filtro demultiplexa i flussi di trasporto e programma MPEG-2 recapitati in modalità push. A partire Windows XP, questo filtro supporta anche i flussi di programma in modalità pull (riproduzione di file). Nelle piattaforme precedenti usare il filtro [mpeg-2 splitter](mpeg-2-splitter.md) per i flussi del programma in modalità pull. Questo filtro può essere usato in qualsiasi tipo di grafico di filtro, incluso un grafico di filtro tv digitale BDA.

> [!Note]  
> Il demultiplexer MPEG-2 non supporta la ricerca accurata dei frame.

 




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | Tutte le modalità:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Filtro IBaseFilter</strong></a></li><li><strong>ISpecifyPropertyPages</strong></li></ul>Solo modalità push:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Tipi di supporti pin di input | Tipo principale: MEDIATYPE_STREAM<br /> Sottotipo:<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>Per altre informazioni, vedere <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.<br /> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | I flussi elementari audio e video devono avere un tipo principale di MEDIATYPE_Audio o MEDIATYPE_Video.<br /> Per altre informazioni, vedere <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.<br /> | 
| Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a>solo modalità push <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl:</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource,</strong></a> <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> Solo modalità pull: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br /> | 
| CLSID del filtro | CLSID_MPEG2Demultiplexer | 
| CLSID pagina delle proprietà | Disponibile solo per i test. Usare <strong>l'interfaccia ISpecifyPropertyPages</strong> per accedere alle pagine delle proprietà | 
| File eseguibile | mpg2splt.ax | 
| <a href="merit.md">Merito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

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

 

 




