---
title: Messaggio MM_MIM_MOREDATA (mmsystem. h)
description: Il \_ \_ messaggio MOREDATA in mm MIM viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora \_ i messaggi di dati MIM abbastanza rapidamente da restare al passo con il driver di dispositivo di input.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048337"
---
# <a name="mm_mim_moredata-message"></a>MM \_ \_ messaggio MOREDATA MIM

Il **messaggio \_ \_ MOREDATA in mm MIM** viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi di [**\_ dati MIM**](mim-data.md) abbastanza rapidamente da restare al passo con il driver di dispositivo di input. La finestra riceve questo messaggio solo quando l'applicazione specifica \_ lo stato di io MIDI \_ nella chiamata alla funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle per il dispositivo di input MIDI che ha ricevuto il messaggio MIDI.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Specifica il messaggio MIDI ricevuto. Il messaggio viene compresso in un valore parola doppia come indicato di seguito:



| Requisito | Valore |
|-----------|-----------------|-----------------------------------------------------|
| Parola alta | Byte di ordine superiore | Non usato.                                           |
|           | Byte di ordine inferiore  | Contiene un secondo byte di dati MIDI (quando necessario).  |
| Parola bassa  | Byte di ordine superiore | Contiene il primo byte dei dati MIDI (quando necessario). |
|           | Byte di ordine inferiore  | Contiene lo stato MIDI.                           |



 

I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Se l'applicazione riceverà dati MIDI più velocemente di quanto possa elaborarla, è consigliabile non usare un meccanismo di callback della finestra. Per ottimizzare la velocità, usare una funzione di callback e usare il messaggio [**\_ MOREDATA MIM**](mim-moredata.md) anziché mm \_ MIM \_ MOREDATA.

Un'applicazione deve eseguire solo una quantità minima di elaborazione dei \_ messaggi MOREDATA MIM di mm \_ . In particolare, le applicazioni non devono chiamare la funzione [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di mm \_ \_MOREDATA MIM). L'applicazione deve invece inserire i dati dell'evento in un buffer e quindi restituire.

Quando un'applicazione riceve un messaggio di [**\_ \_ dati MIM di mm**](mm-mim-data.md) dopo una serie \_ di \_ messaggi MOREDATA MIM, ha rilevato gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo di tempo.

Lo stato dell'esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato; ogni messaggio viene espanso in modo da includere il byte di stato MIDI.

Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI. Nessun timestamp disponibile con questo messaggio. Per i dati di input con timestamp, è necessario utilizzare i messaggi inviati alle funzioni di callback.

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

 

