---
title: Messaggio WM_POINTERROUTEDTO
description: Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, esegue la transizione da un processo a un altro tra i contenuti configurati per il concatenamento tra processi (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERROUTEDTO
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
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400500"
---
# <a name="wm_pointerroutedto-message"></a>Messaggio WM_POINTERROUTEDTO

Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, esegue la transizione da un processo a un altro tra i contenuti configurati per il concatenamento tra processi ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Questo messaggio viene inviato al processo che non riceve attualmente l'input del puntatore.


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

Questo messaggio non viene inviato quando viene pubblicato un messaggio di [**WM_POINTERDOWN**](wm-pointerdown.md) per un nuovo ID puntatore in un processo diverso.

Se un messaggio di **WM_POINTERROUTEDTO** viene pubblicato per primo, un messaggio di [**WM_POINTERDOWN**](wm-pointerdown.md) non viene inviato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

