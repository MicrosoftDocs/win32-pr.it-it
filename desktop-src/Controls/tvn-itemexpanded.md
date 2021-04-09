---
title: Codice di notifica TVN_ITEMEXPANDED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco di elementi figlio di un elemento padre è espanso o compresso. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMEXPANDED
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121282"
---
# <a name="tvn_itemexpanded-notification-code"></a>\_Codice di notifica ITEMEXPANDED di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco di elementi figlio di un elemento padre è espanso o compresso. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento padre nei membri **Hite**, **state** e **lParam** . Il membro dell' **azione** indica se l'elenco è espanso o compresso. Per un elenco di valori possibili, vedere la descrizione del messaggio [**di \_ espansione TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDEDW** (Unicode) e **TVN \_ ITEMEXPANDEDA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ITEMEXPANDING TVN](tvn-itemexpanding.md)
</dt> </dl>

 

 





