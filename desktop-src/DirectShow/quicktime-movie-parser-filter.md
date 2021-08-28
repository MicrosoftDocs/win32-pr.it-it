---
description: Filtro del parser di film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro del parser di film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a65ba14cb748eb10c6afddf3e4747f11d68a4f9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476717"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro del parser di film QuickTime

Questo componente è stato rimosso da Windows Vista e sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

Il filtro QuickTime Movie Parser suddivide i dati ® QuickTime® Apple in flussi audio e video. Supporta QuickTime 2.0 e versioni precedenti. Il pin di input si connette a un filtro di origine, ad esempio il filtro [Origine file](file-source--async--filter.md) asincrona o il filtro Origine [file URL.](file-source--url--filter.md) Il parser usa il [filtro AVI Decompressor](avi-decompressor-filter.md) o [QT Decompressor](qt-decompressor-filter.md) per decomprimere i file QuickTime. Il filtro crea un pin di output per il flusso video e un pin di output per il flusso audio.




| | | Interfacce di filtro | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipi di supporti pin di input | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipi di supporti pin di output | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | | Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare clsID | CLSID_QuickTimeParser | | Proprietà pagina CLSID | Nessuna pagina delle proprietà. | | File eseguibili | quartz.dll | | <a href="merit.md">|</a> MERIT_NORMAL | | <a href="filter-categories.md">Filtro categoria |</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



