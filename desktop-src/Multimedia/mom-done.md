---
title: MOM_DONE messaggio (Mciapi.h)
description: Il messaggio MOM DONE viene inviato a una funzione di callback di output MIDI quando viene riprodotto il buffer esclusivo di sistema o di flusso specificato e viene \_ restituito all'applicazione.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4361ef25af7bab629138d4371c852d661373891e9d9513ae30b8ad79e97670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807031"
---
# <a name="mom_done-message"></a>Messaggio MOM \_ DONE

Il **messaggio MOM \_ DONE** viene inviato a una funzione di callback di output MIDI quando viene riprodotto il buffer esclusivo di sistema o di flusso specificato e viene restituito all'applicazione.


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a [**una struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Riservato; non utilizzare .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

