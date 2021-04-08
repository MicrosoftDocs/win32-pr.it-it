---
title: Codice di notifica LVN_KEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata premuta una chiave. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- Controlli di Windows per il codice di notifica LVN_KEYDOWN
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965011"
---
# <a name="lvn_keydown-notification-code"></a>\_Codice di notifica KeyDown LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata premuta una chiave. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





