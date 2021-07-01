---
title: MIM_DATA messaggio (Mmsystem.h)
description: Il messaggio MIM DATA viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene \_ ricevuto da un dispositivo di input MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA message Windows Multimedia
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
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118406"
---
# <a name="mim_data-message"></a>Messaggio DATI \_ MIM

Il **messaggio MIM \_ DATA** viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Messaggio MIDI ricevuto. Il messaggio viene inserito in un valore doubleword come indicato di seguito:



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

Ora di ricezione del messaggio da parte del driver di dispositivo di input. Il timestamp è specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.

Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI.

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

 

