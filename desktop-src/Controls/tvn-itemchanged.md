---
title: Codice di notifica TVN_ITEMCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento sono stati modificati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873881"
---
# <a name="tvn_itemchanged-notification-code"></a>\_Codice di notifica ITEMCHANGED di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento sono stati modificati. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) che descrive l'elemento modificato. Il membro **uChanged** è impostato \_ sullo stato TVIF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **false** per accettare la modifica o **true** per impedire la modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) e **TVN \_ ITEMCHANGEDA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ITEMCHANGING TVN](tvn-itemchanging.md)
</dt> </dl>

 

 





