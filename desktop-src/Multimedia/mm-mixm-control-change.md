---
title: Messaggio MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: Il \_ \_ messaggio di modifica del controllo MIXM mm \_ viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di un controllo associato a una linea audio è stato modificato. L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per il controllo specificato.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302025"
---
# <a name="mm_mixm_control_change-message"></a>MM \_ \_ messaggio di \_ modifica controllo MIXM

Il messaggio di **\_ \_ \_ modifica del controllo MIXM mm** viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di un controllo associato a una linea audio è stato modificato. L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per il controllo specificato.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Handle per il dispositivo mixer (**HMIXER**) che ha inviato il messaggio di notifica.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

Identificatore di controllo per il controllo mixer con stato modificato. Questo identificatore corrisponde al membro **dwControlID** della struttura **MIXERCONTROL** restituita dalla funzione **mixerGetlineControls**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione deve aprire un dispositivo mixer e specificare una finestra di callback per ricevere il messaggio di **\_ \_ \_ modifica del controllo MIXM mm** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mixer audio](audio-mixers.md)
</dt> <dt>

[Messaggi mixer audio](audio-mixer-messages.md)
</dt> </dl>

 

 





