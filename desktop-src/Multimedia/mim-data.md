---
title: MIM_DATA messaggio (Mmsystem.h)
description: Il MIM data viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo \_ di input MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA messaggio Windows Multimediali
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
ms.openlocfilehash: bebbb9ca6016706605de8fed29e5fa5ebaf6055f4a730fb563323f306606b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137290"
---
# <a name="mim_data-message"></a>\_MIM Messaggio DATA

Il **MIM \_ data** viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.


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
|           | Byte in ordine ridotto  | Contiene un secondo byte di dati MIDI (quando necessario).  |
| Parola bassa  | Byte di ordine elevato | Contiene il primo byte di dati MIDI (se necessario). |
|           | Byte in ordine ridotto  | Contiene lo stato MIDI.                           |



 

I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Ora in cui il messaggio è stato ricevuto dal driver del dispositivo di input. Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la [**funzione midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

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
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MidI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

