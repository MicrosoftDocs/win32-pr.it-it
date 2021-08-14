---
title: MM_MOM_POSITIONCB messaggio (Mmsystem.h)
description: Il messaggio MM MOM POSITIONCB viene inviato a una finestra quando viene raggiunto un evento \_ \_ CALLBACK F MEVT \_ nel flusso di output \_ MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f68afecddd9b6ca8a0e5f6305b430b059b93db5a2abb966c0a7aed9ab350f7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807161"
---
# <a name="mm_mom_positioncb-message"></a>Messaggio \_ MM MOM \_ POSITIONCB

Il **messaggio MM MOM \_ \_ POSITIONCB** viene inviato a una finestra quando viene raggiunto un evento CALLBACK F MEVT \_ nel flusso di output \_ MIDI.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a una [**struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica l'evento che ha causato il callback. Il **membro dwOffset** fornisce l'offset dell'evento.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Riservato; non utilizzare .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

La riproduzione del buffer del flusso continua anche durante l'esecuzione della funzione di callback. Tutti gli eventi dopo l'evento MEVT F CALLBACK nel buffer verranno pianificati e inviati in tempo indipendentemente dal tempo impiegato nella \_ \_ funzione di callback.

Se i callback di posizione vengono generati più rapidamente di quanto l'applicazione possa elaborarli, il membro **dwOffset** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) potrebbe fare riferimento a un evento che l'applicazione non ha ancora elaborato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

