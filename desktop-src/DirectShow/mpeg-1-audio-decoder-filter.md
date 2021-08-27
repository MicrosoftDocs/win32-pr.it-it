---
description: Filtro decodificatore audio MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro decodificatore audio MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3c014497d8b3db5aaf3031250e78edd8b59cb2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983824"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Filtro decodificatore audio MPEG-1

Decodifica l'audio MPEG-1 di livello I e di livello II in PCM.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | 
| Tipi di supporti pin di input | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Sono validi i sottotipi seguenti:<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | 
| Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID del filtro | CLSID_CMpegAudioCodec | 
| CLSID pagina delle proprietà | CLSID_MpegAudioDecoderPropertyPage | 
| File eseguibile | quartz.dll | 
| <a href="merit.md">Merito</a> | 0x03680001 | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




