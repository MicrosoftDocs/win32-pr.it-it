---
description: Filtro del parser di film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro del parser di film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0028b604efe31749144ca98cb80057685ed0c1db
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983614"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro del parser di film QuickTime

Questo componente è stato rimosso da Windows Vista e sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

Il filtro QuickTime Movie Parser suddivide i dati ® QuickTime® in flussi audio e video. Supporta QuickTime 2.0 e versioni precedenti. Il pin di input si connette a un filtro di origine, ad esempio il filtro [Origine file](file-source--async--filter.md) asincrona o il filtro Origine [file URL.](file-source--url--filter.md) Il parser usa il [filtro AVI Decompressor](avi-decompressor-filter.md) o [QT Decompressor](qt-decompressor-filter.md) per decomprimere i file QuickTime. Il filtro crea un pin di output per il flusso video e un pin di output per il flusso audio.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a> | 
| Tipi di supporti pin di input | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | 
| Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID del filtro | CLSID_QuickTimeParser | 
| CLSID pagina delle proprietà | Nessuna pagina delle proprietà. | 
| File eseguibile | quartz.dll | 
| <a href="merit.md">Merito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



