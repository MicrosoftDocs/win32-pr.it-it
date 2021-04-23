---
description: Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro parser MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro renderer MIDI (Windows.devices.midi.h)
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
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909409"
---
# <a name="midi-renderer-filter"></a>Filtro renderer MIDI

Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro [parser MIDI.](midi-parser-filter.md)



| Label | Valore |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMClockSlave,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicAudio,**](/windows/desktop/api/Control/nn-control-ibasicaudio) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                                                                                                                  |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Tipi di supporti pin di output                   | Non applicabile                                                                                                                                                                                                                                                                                                                                                                       |
| Interfacce pin di output                    | Non applicabile                                                                                                                                                                                                                                                                                                                                                                       |
| Filtro CLSID                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                                                                                                                                                                                                     |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ PREFERITO                                                                                                                                                                                                                                                                                                                                                                     |
| [Categoria filtro](filter-categories.md) | CLSID \_ MidiRendererCategory                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il GUID per il tipo di formato è **NULL,** ma il blocco di formato contiene la struttura seguente:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Il **membro dwDivision** specifica la divisione temporale del file. La divisione temporale viene specificata nell'intestazione di qualsiasi file MIDI standard (SMF) nel `MThd` blocco . Il renderer MIDI imposta questa proprietà nel flusso di dati MIDI chiamando la **funzione midiStreamProperty.**

Gli esempi del filtro del parser MIDI contengono un secondo di dati MIDI. Il renderer MIDI usa la **funzione midiStreamOut** per eseguire il rendering dei dati MIDI. Ogni esempio è un punto di sincronizzazione: l'inizio del buffer contiene tutti i comandi necessari per impostare lo stato corretto per il rendering del buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Windows.devices.midi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 




