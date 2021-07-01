---
title: MM_MIM_DATA messaggio (Mmsystem.h)
description: Il messaggio MM \_ MIM \_ DATA viene inviato a una finestra quando un messaggio MIDI completo viene ricevuto da un dispositivo di input MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119696"
---
# <a name="mm_mim_data-message"></a>Messaggio MM \_ MIM \_ DATA

Il **messaggio MM \_ MIM \_ DATA** viene inviato a una finestra quando un messaggio MIDI completo viene ricevuto da un dispositivo di input MIDI.


```C++
MM_MIM_DATA 
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

Messaggio MIDI ricevuto. Il messaggio viene inserito in un valore doubleword come indicato di seguito:



| Requisito | Valore | Descrizione |
|-----------|-----------------|-----------------------------------------------------|
| Parola alta | Byte di ordine elevato | Non usato.                                           |
|           | Byte in ordine ridotto  | Contiene un secondo byte di dati MIDI (quando necessario).  |
| Parola bassa  | Byte di ordine elevato | Contiene il primo byte di dati MIDI (se necessario). |
|           | Byte in ordine ridotto  | Contiene lo stato MIDI.                           |



 

I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.

Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI. Con questo messaggio non è disponibile alcun timestamp. Per i dati di input con timestamp, è necessario usare i messaggi inviati alle funzioni di callback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[MidI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

 





