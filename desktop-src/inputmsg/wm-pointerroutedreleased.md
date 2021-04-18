---
title: Messaggio WM_POINTERROUTEDRELEASED
description: Inviato a tutti i processi (configurato per il concatenamento tra processi tramite AddContentWithCrossProcessChaining e non gestisce l'input del puntatore) mai associato a un ID puntatore specifico, quando viene ricevuto un messaggio di WM_POINTERUP nel processo corrente.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERROUTEDRELEASED
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
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400637"
---
# <a name="wm_pointerroutedreleased-message"></a>Messaggio WM_POINTERROUTEDRELEASED

Inviato a tutti i processi (configurato per il concatenamento tra processi tramite [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e non gestisce l'input del puntatore) mai associato a un ID puntatore specifico, quando viene ricevuto un messaggio di [**WM_POINTERUP**](wm-pointerup.md) nel processo corrente.


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
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

