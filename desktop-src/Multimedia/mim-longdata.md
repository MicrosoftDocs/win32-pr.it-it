---
title: MIM_LONGDATA messaggio (Mmsystem.h)
description: Il MIM LONGDATA viene inviato a una funzione di callback di input MIDI quando un buffer esclusivo di sistema è stato riempito con dati e viene \_ restituito all'applicazione.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA messaggio Windows Multimediali
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
ms.openlocfilehash: 82605835ce8ac231346014215c854abfe9ae7a55fd81e81b8d6214fb8a230327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137212"
---
# <a name="mim_longdata-message"></a>\_MIM Messaggio LONGDATA

Il **MIM \_ LONGDATA** viene inviato a una funzione di callback di input MIDI quando un buffer esclusivo di sistema è stato riempito con dati e viene restituito all'applicazione.


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a [**una struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer di input.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Ora in cui i dati sono stati ricevuti dal driver del dispositivo di input. Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la [**funzione midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il buffer restituito potrebbe non essere pieno. Per determinare il numero di byte registrati nel buffer restituito, usare il **membro dwBytesRecorded** della [**struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) specificata da *lpMidiHdr*.

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

 

