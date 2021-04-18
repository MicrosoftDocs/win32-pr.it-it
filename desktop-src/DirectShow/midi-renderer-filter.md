---
description: Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro del parser MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro renderer MIDI (Windows. Devices. MIDI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331434"
---
# <a name="midi-renderer-filter"></a>Filtro renderer MIDI

Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro del [parser MIDI](midi-parser-filter.md) .



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                                                                                                                  |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Tipi di supporti pin di output                   | Non applicabile                                                                                                                                                                                                                                                                                                                                                                       |
| Interfacce del PIN di output                    | Non applicabile                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID filtro                             | \_AVIMIDIRENDER CLSID                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                                                                                                                                                                                                     |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | \_preferenza preferita                                                                                                                                                                                                                                                                                                                                                                     |
| [Categoria filtro](filter-categories.md) | \_MIDIRENDERERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il GUID per il tipo di formato è **null**, ma il blocco di formato contiene la struttura seguente:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Il membro **dwDivision** specifica la divisione dell'ora del file. La divisione temporale viene specificata nell'intestazione di qualsiasi file MIDI standard (SMF), nel `MThd` blocco. Il renderer MIDI imposta questa proprietà sul flusso di dati MIDI chiamando la funzione **midiStreamProperty** .

Gli esempi del filtro del parser MIDI contengono un secondo di dati MIDI. Il renderer MIDI usa la funzione **midiStreamOut** per eseguire il rendering dei dati MIDI. Ogni esempio è un punto di sincronizzazione: l'inizio del buffer contiene tutti i comandi necessari per impostare lo stato corretto per il rendering del buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Windows. Devices. MIDI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




