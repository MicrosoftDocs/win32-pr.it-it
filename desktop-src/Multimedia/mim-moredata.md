---
title: MIM_MOREDATA messaggio (Mmsystem.h)
description: Il messaggio MIM MOREDATA viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi MIM DATA abbastanza velocemente da restare al passo con il driver di dispositivo di \_ \_ input.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA di Windows multimediali
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
ms.openlocfilehash: 130a07d1d205e9944c7be6ab9ad1294e09d0ebdcdb81d5befc5468ff5a65218f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782971"
---
# <a name="mim_moredata-message"></a>\_MIM MESSAGGIO MOREDATA

Il messaggio **\_ MIM MOREDATA** viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi [**MIM \_ DATA in**](mim-data.md) modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di input. La funzione di callback riceve questo messaggio solo quando l'applicazione specifica MIDI IO STATUS nella chiamata \_ \_ alla funzione [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Specifica il messaggio MIDI ricevuto. Il messaggio viene inserito in un **valore DWORD** come indicato di seguito:



| Requisito | Valore | Descrizione |
|-----------|-----------------|-----------------------------------------------------|
| Parola alta | Byte di ordine elevato | Non usato.                                           |
|           | Byte di ordine ridotto  | Contiene un secondo byte di dati MIDI (quando necessario).  |
| Parola bassa  | Byte di ordine elevato | Contiene il primo byte dei dati MIDI (quando necessario). |
|           | Byte di ordine ridotto  | Contiene lo stato MIDI.                           |



 

I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Specifica l'ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input. Il timestamp viene specificato in millisecondi, a partire da 0 quando è stata chiamata la funzione [**midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Un'applicazione deve eseguire solo una quantità minima di elaborazione MIM \_ messaggi MOREDATA. In particolare, le applicazioni non devono chiamare la [funzione PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione MIM \_ MOREDATA. Al contrario, l'applicazione deve inserire i dati dell'evento in un buffer e quindi restituire .

Quando un'applicazione riceve un messaggio [**MIM \_ DATA**](mim-data.md) dopo una serie di messaggi MOREDATA di MIM, ha raggiunto gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo di \_ tempo.

Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.

Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Instrument Digital Interface (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

