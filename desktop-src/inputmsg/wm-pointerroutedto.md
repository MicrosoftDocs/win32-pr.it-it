---
title: WM_POINTERROUTEDTO messaggio
description: Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, passa da un processo a un altro attraverso il contenuto configurato per il concatenamento tra processi (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO messaggi di input e notifiche
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9b7de7dd1affb9100a29613e3b4186d3d5bdaa32d853e683579fdcc62e7f981f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695622"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO messaggio

Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, passa da un processo a un altro attraverso il contenuto configurato per il concatenamento tra processi ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Questo messaggio viene inviato al processo che attualmente non riceve l'input del puntatore.


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

NULL

## <a name="remarks"></a>Commenti

Questo messaggio non viene inviato quando viene pubblicato [**WM_POINTERDOWN**](wm-pointerdown.md) messaggio per un nuovo ID puntatore in un processo diverso.

Un [**WM_POINTERDOWN**](wm-pointerdown.md) messaggio non viene inviato se **viene WM_POINTERROUTEDTO** un messaggio di posta elettronica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

