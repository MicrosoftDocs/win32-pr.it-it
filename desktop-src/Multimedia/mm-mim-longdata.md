---
title: MM_MIM_LONGDATA messaggio (Mmsystem.h)
description: Il messaggio MM MIM LONGDATA viene inviato a una finestra quando viene ricevuto un messaggio esclusivo di sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del \_ \_ sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4748381500f42a5dc4f2bceae8ad862a64f237c9d5024e4b0b7cc96a694e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065521"
---
# <a name="mm_mim_longdata-message"></a>MESSAGGIO DI \_ MIM \_ LONGDATA

Il **messaggio MM MIM \_ \_ LONGDATA** viene inviato a una finestra quando viene ricevuto un messaggio esclusivo di sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle per il dispositivo di input MIDI che ha ricevuto i dati.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a [**una struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il buffer restituito potrebbe non essere pieno. Per determinare il numero di byte registrati nel buffer restituito, usare il membro **dwBytesRecorded** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) a cui punta *lpMidiHdr*.

Con questo messaggio non è disponibile alcun timestamp. Per i dati di input con timestamp, è necessario usare i messaggi inviati alle funzioni di callback.

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

 

