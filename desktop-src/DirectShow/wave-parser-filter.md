---
description: Filtro del parser WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro del parser WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91508500b02743f7cac8b4ed5cff718d12e3b03
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987854"
---
# <a name="wave-parser-filter"></a>Filtro del parser WAVE

Il filtro del parser WAVE analizza i dati audio in formato WAV da file wav, au o aif. Il filtro upstream deve essere il filtro [origine](file-source--async--filter.md) file asincrona, il filtro origine [file URL](file-source--url--filter.md) o un filtro di origine asincrono di terze parti compatibile che contiene dati audio WAV. Il flusso di output è dato da dati audio, che è possibile connettere direttamente a un filtro di rendering audio o a un filtro di trasformazione audio.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a> | 
| Tipi di supporti pin di input | Tipo principale: MEDIATYPE_StreamThe seguenti sottotipi validi:<br /><ul><li>MEDIASUBTYPE_AIFF</li><li>MEDIASUBTYPE_AU</li><li>MEDIASUBTYPE_WAVE</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | Tipo principale: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM o un altro tipo di compressione. Vedere <a href="audio-subtypes.md"><strong>Sottotipi audio.</strong></a><br /> Tipo di formato: FORMAT_WaveFormatEx<br /> | 
| Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| CLSID del filtro | {D51BD5A1-7548-11cf-A520-0080C77EF58A} | 
| CLSID pagina delle proprietà | Nessuna pagina delle proprietà. | 
| File eseguibile | quartz.dll | 
| <a href="merit.md">Merito</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Questo filtro supporta i tipi di file seguenti:

-   WAVE (.wav)
-   AIFF e AIFF-C (.aif)
-   Au (.au)

Tuttavia, presenta le limitazioni seguenti per il formato audio:

-   L'audio deve essere PCM lineare a 8 o 16 bit.
-   Per i file AIFF-C, l'audio deve essere non compresso, in ordine di byte big endian (tipo di compressione 'NONE').

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




