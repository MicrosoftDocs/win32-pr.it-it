---
title: Messaggio MM_WOM_OPEN (mmsystem. h)
description: Il \_ \_ messaggio di apertura mm WOM viene inviato a una finestra quando viene aperto il dispositivo di output della forma d'onda specificata.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121663"
---
# <a name="mm_wom_open-message"></a>MM \_ WOM \_ messaggio aperto

Il messaggio di **\_ \_ apertura mm WOM** viene inviato a una finestra quando viene aperto il dispositivo di output della forma d'onda specificata.


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle per il dispositivo che è stato aperto.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Audio Waveform](waveform-audio.md)
</dt> <dt>

[Messaggi di forma d'onda](waveform-messages.md)
</dt> </dl>

 

 





