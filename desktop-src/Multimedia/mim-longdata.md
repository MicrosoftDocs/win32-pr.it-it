---
title: Messaggio MIM_LONGDATA (mmsystem. h)
description: Il \_ messaggio LONGDATA MIM viene inviato a una funzione di callback input MIDI quando un buffer esclusivo del sistema è stato riempito con i dati e viene restituito all'applicazione.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121670"
---
# <a name="mim_longdata-message"></a>\_Messaggio LONGDATA MIM

Il **messaggio \_ LONGDATA MIM** viene inviato a una funzione di callback input MIDI quando un buffer esclusivo del sistema è stato riempito con i dati e viene restituito all'applicazione.


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer di input.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Tempo durante il quale i dati sono stati ricevuti dal driver di dispositivo di input. Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il buffer restituito potrebbe non essere pieno. Per determinare il numero di byte registrati nel buffer restituito, usare il membro **dwBytesRecorded** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) specificata da *lpMidiHdr*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MIDI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

