---
title: Codice di notifica TVN_ITEMCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento stanno per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517824"
---
# <a name="tvn_itemchanging-notification-code"></a>\_Codice di notifica ITEMCHANGING di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento stanno per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) che descrive l'elemento in corso di modifica. Il membro **uChanged** è impostato \_ sullo stato TVIF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **false** per accettare la modifica o **true** per impedire la modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) e **TVN \_ ITEMCHANGINGA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ITEMCHANGED TVN](tvn-itemchanged.md)
</dt> </dl>

 

 





