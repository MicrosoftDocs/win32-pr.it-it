---
title: WM_POINTERROUTEDRELEASED messaggio
description: Inviato a tutti i processi (configurati per il concatenamento tra processi tramite AddContentWithCrossProcessChaining e che attualmente non gestisce l'input del puntatore) associati a un ID puntatore specifico, quando viene ricevuto un messaggio WM_POINTERUP nel processo corrente.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED messaggi di input e notifiche del messaggio
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 318134779d94824daef0b05903f45121665892fbcafbeb48589ef150f324d2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611291"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED messaggio

Inviato a tutti i processi (configurati per il concatenamento tra processi tramite [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e che attualmente non gestisce l'input del puntatore) associati a un ID puntatore specifico, quando viene ricevuto un messaggio [**WM_POINTERUP**](wm-pointerup.md) nel processo corrente.


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

