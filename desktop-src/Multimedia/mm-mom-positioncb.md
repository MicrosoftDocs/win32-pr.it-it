---
title: Messaggio MM_MOM_POSITIONCB (mmsystem. h)
description: Il \_ messaggio mm MOM \_ POSITIONCB viene inviato a una finestra quando \_ viene raggiunto un evento di callback F MEVT \_ nel flusso di output MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB messaggi multimediali di Windows
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
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963823"
---
# <a name="mm_mom_positioncb-message"></a>MM \_ \_ POSITIONCB messaggio MOM

Il messaggio **mm \_ MOM \_ POSITIONCB** viene inviato a una finestra quando \_ viene raggiunto un evento di callback F MEVT \_ nel flusso di output MIDI.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica l'evento che ha causato il callback. Il membro **dwOffset** restituisce l'offset dell'evento.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Riservati Non usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

La riproduzione del buffer del flusso continua anche mentre la funzione di callback è in esecuzione. Tutti gli eventi dopo l' \_ \_ evento di callback F MEVT nel buffer verranno pianificati e inviati in tempo indipendentemente dalla quantità di tempo impiegato nella funzione di callback.

Se i callback di posizione vengono generati più rapidamente di quanto l'applicazione possa elaborarli, il membro **dwOffset** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) può fare riferimento a un evento che l'applicazione non ha ancora elaborato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

