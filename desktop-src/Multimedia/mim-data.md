---
title: Messaggio MIM_DATA (mmsystem. h)
description: Il \_ messaggio di dati MIM viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874630"
---
# <a name="mim_data-message"></a>\_Messaggio dati MIM

Il messaggio di **\_ dati MIM** viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Messaggio MIDI ricevuto. Il messaggio viene compresso in un valore parola doppia come indicato di seguito:



| Requisito | Valore |
|-----------|-----------------|-----------------------------------------------------|
| Parola alta | Byte di ordine superiore | Non usato.                                           |
|           | Byte di ordine inferiore  | Contiene un secondo byte di dati MIDI (quando necessario).  |
| Parola bassa  | Byte di ordine superiore | Contiene il primo byte dei dati MIDI (quando necessario). |
|           | Byte di ordine inferiore  | Contiene lo stato MIDI.                           |



 

I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input. Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Lo stato dell'esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato; ogni messaggio viene espanso in modo da includere il byte di stato MIDI.

Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI.

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

 

