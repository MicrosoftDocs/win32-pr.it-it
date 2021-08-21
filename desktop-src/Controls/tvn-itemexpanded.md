---
title: TVN_ITEMEXPANDED di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che l'elenco di elementi figlio di un elemento padre è stato espanso o compresso. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED del codice di notifica Windows controlli
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
ms.openlocfilehash: 18af761c7580707bfd0926874e25069ca15b564bf6ef205cd6dc7aaaecb6a772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018629"
---
# <a name="tvn_itemexpanded-notification-code"></a>Codice di \_ notifica TVN ITEMEXPANDED

Notifica alla finestra padre di un controllo visualizzazione albero che l'elenco di elementi figlio di un elemento padre è stato espanso o compresso. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Il **membro itemNew** è una [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento padre nei membri **hItem**, **state** e **lParam.** Il **membro** azione indica se l'elenco è espanso o compresso. Per un elenco dei valori possibili, vedere la descrizione del messaggio [**TVM \_ EXPAND.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDEDW** (Unicode) e **\_ TVN ITEMEXPANDEDA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)
</dt> </dl>

 

 





