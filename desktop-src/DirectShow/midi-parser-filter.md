---
description: Filtro parser MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro parser MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5907c36e668a39494b46ec6bbc67e4d8cb4870357df9c1f0303c882bc86f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256511"
---
# <a name="midi-parser-filter"></a>Filtro parser MIDI

Il filtro del parser MIDI legge i dati MIDI disponibili in . MID e . File RMI. Il filtro accetta un [](file-source--async--filter.md) flusso dai filtri Origine file asincrona o Origine [file URL](file-source--url--filter.md) e restituisce gli esempi MIDI al [**renderer MIDI**](midi-renderer-filter.md) per la riproduzione.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipi di supporti pin di input                    | Flusso \_ MEDIATYPE, MEDIASUBTYPE \_ Midi                                                                    |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL                                                                      |
| Interfacce pin di output                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID del filtro                             | CLSID \_ MIDIParser                                                                                        |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                         |
| File eseguibile                               | quartz.dll                                                                                               |
| [Merito](merit.md)                       | PROBABILITÀ \_ IMPROBABILE                                                                                          |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere [**Renderer MIDI.**](midi-renderer-filter.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



