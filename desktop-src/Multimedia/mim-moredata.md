---
title: Messaggio MIM_MOREDATA (mmsystem. h)
description: Il \_ messaggio MOREDATA MIM viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora \_ i messaggi di dati MIM in modo sufficientemente veloce da restare al passo con il driver di dispositivo di input.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743930"
---
# <a name="mim_moredata-message"></a>\_Messaggio MOREDATA MIM

Il **messaggio \_ MOREDATA MIM** viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi di [**\_ dati MIM**](mim-data.md) in modo sufficientemente veloce da restare al passo con il driver di dispositivo di input. La funzione di callback riceve questo messaggio solo quando l'applicazione specifica \_ lo stato di io MIDI \_ nella chiamata alla funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Specifica il messaggio MIDI ricevuto. Il messaggio viene compresso in un valore **DWORD** come indicato di seguito:



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

Specifica l'ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input. Il timestamp viene specificato in millisecondi, a partire da 0 quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'applicazione deve eseguire solo una quantità minima di elaborazione dei \_ messaggi MOREDATA MIM. In particolare, le applicazioni non devono chiamare la funzione [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di MIM \_ MOREDATA.) L'applicazione deve invece inserire i dati dell'evento in un buffer e quindi restituire.

Quando un'applicazione riceve un messaggio di [**\_ dati MIM**](mim-data.md) dopo una serie di \_ messaggi MOREDATA MIM, ha rilevato gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo di tempo.

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

 

