---
title: TVN_ITEMEXPANDING codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che l'elenco di elementi figlio di un elemento padre sta per espandersi o comprimere. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f4403b41682590d305b527d6445c208011b368b2d2474d66720ed32d29c80ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957790"
---
# <a name="tvn_itemexpanding-notification-code"></a>Codice di \_ notifica TVN ITEMEXPANDING

Notifica alla finestra padre di un controllo visualizzazione albero che l'elenco di elementi figlio di un elemento padre sta per espandersi o comprimere. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Il **membro itemNew** è una [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento padre nei membri **hItem**, **state** e **lParam.** Il **membro** azione indica se l'elenco deve essere espanso o compresso. Per un elenco dei valori possibili, vedere la descrizione del [**messaggio TVM \_ EXPAND.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per impedire l'espansione o la compressione dell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) e **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 





