---
title: Messaggio MOM_POSITIONCB (mmsystem. h)
description: Il \_ messaggio di posizione MOM viene inviato quando \_ \_ viene raggiunto un evento di callback MEVT F nel flusso di output MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743354"
---
# <a name="mom_positioncb-message"></a>\_Messaggio MOM POSITIONCB

Il messaggio di **\_ posizione MOM** viene inviato quando viene raggiunto un evento di **\_ \_ callback MEVT F** nel flusso di output MIDI.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer di input.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

La riproduzione del buffer del flusso continua anche mentre la funzione di callback è in esecuzione. Tutti gli eventi dopo l'evento di **\_ \_ callback F MEVT** nel buffer verranno pianificati e inviati in tempo indipendentemente dalla quantità di tempo impiegato nella funzione di callback.

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

 

