---
description: Filtro del parser MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro del parser MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965485"
---
# <a name="midi-parser-filter"></a>Filtro del parser MIDI

Il filtro del parser MIDI legge i dati MIDI presenti in. MID e. File RMI. Il filtro accetta un flusso dall' [origine file asincrona](file-source--async--filter.md) o i filtri [origine file URL](file-source--url--filter.md) e restituisce esempi MIDI al [**renderer MIDI**](midi-renderer-filter.md) per la riproduzione.



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipi di supporti pin di input                    | \_Flusso MEDIATYPE, MEDIASUBTYPE \_ MIDI                                                                    |
| Interfacce pin di input                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipi di supporti pin di output                   | MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null                                                                      |
| Interfacce del PIN di output                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID filtro                             | \_MIDIPARSER CLSID                                                                                        |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                         |
| File eseguibile                               | quartz.dll                                                                                               |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                          |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                            |



 

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere [**renderer MIDI**](midi-renderer-filter.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



