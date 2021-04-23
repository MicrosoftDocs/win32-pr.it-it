---
description: Filtro parser MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro parser MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908429"
---
# <a name="midi-parser-filter"></a>Filtro del parser MIDI

Il filtro midi parser legge i dati MIDI trovati in . MID e . File RMI. Il filtro accetta un flusso dai filtri [Origine file](file-source--async--filter.md) asincrona o Origine [file URL](file-source--url--filter.md) e restituisce gli esempi MIDI al [**renderer MIDI**](midi-renderer-filter.md) per la riproduzione.



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipi di supporti pin di input                    | Flusso \_ MEDIATYPE, MEDIASUBTYPE \_ Midi                                                                    |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL                                                                      |
| Interfacce pin di output                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtro CLSID                             | CLSID \_ MIDIParser                                                                                        |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                         |
| File eseguibile                               | quartz.dll                                                                                               |
| [Merito](merit.md)                       | PROBABILITÀ \_ IMPROBABILE                                                                                          |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere [**Renderer MIDI.**](midi-renderer-filter.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 



