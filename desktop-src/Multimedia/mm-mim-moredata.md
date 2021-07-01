---
title: MM_MIM_MOREDATA messaggio (Mmsystem.h)
description: Il messaggio MM MIM MOREDATA viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI ma l'applicazione non elabora i messaggi MIM DATA in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di \_ \_ \_ input.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA messaggio Windows Multimedia
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
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120026"
---
# <a name="mm_mim_moredata-message"></a>Mm \_ MIM \_ MOREDATA message

Il messaggio **MM \_ MIM \_ MOREDATA** viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI ma l'applicazione non elabora i messaggi [**MIM \_ DATA**](mim-data.md) in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di input. La finestra riceve questo messaggio solo quando l'applicazione specifica MIDI \_ IO STATUS nella chiamata alla funzione \_ [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)


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

Specifica il messaggio MIDI ricevuto. Il messaggio viene inserito in un valore doubleword come indicato di seguito:



| Requisito | Valore | Descrizione |
|-----------|-----------------|-----------------------------------------------------|
| Parola alta | Byte di ordine elevato | Non usato.                                           |
|           | Byte di ordine ridotto  | Contiene un secondo byte di dati MIDI (quando necessario).  |
| Parola bassa  | Byte di ordine elevato | Contiene il primo byte dei dati MIDI (quando necessario). |
|           | Byte di ordine ridotto  | Contiene lo stato MIDI.                           |



 

I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Se l'applicazione riceverà i dati MIDI più velocemente di quanto possa elaborarlo, non è consigliabile usare un meccanismo di callback della finestra. Per ottimizzare la velocità, usare una funzione di callback e usare il messaggio [**\_ MIM MOREDATA**](mim-moredata.md) anziché MM \_ MIM \_ MOREDATA.

Un'applicazione deve eseguire solo una quantità minima di elaborazione dei messaggi MM \_ MIM \_ MOREDATA. In particolare, le applicazioni non devono chiamare la [funzione PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di MM \_ MIM \_ MOREDATA. Al contrario, l'applicazione deve inserire i dati dell'evento in un buffer e quindi restituire .

Quando un'applicazione riceve un messaggio [**MM \_ MIM \_ DATA**](mm-mim-data.md) dopo una serie di messaggi MM \_ MIM MOREDATA, ha raggiunto gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo \_ di tempo.

Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.

Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI. Con questo messaggio non è disponibile alcun timestamp. Per i dati di input con timestamp, è necessario usare i messaggi inviati alle funzioni di callback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Instrument Digital Interface (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

