---
title: TVN_BEGINDRAG di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che è in corso un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95952ee42dfe8eb8dd1a46c66dcd452f41cbc9723fa175c2a0d1fc75056c31ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957920"
---
# <a name="tvn_begindrag-notification-code"></a>Codice di notifica \_ TVN BEGINDRAG

Notifica alla finestra padre di un controllo visualizzazione albero che è in corso un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Il **membro itemNew** è una [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento trascinato nei membri **hItem**, **state** e **lParam.** Il **membro ptDrag** specifica le coordinate dello schermo correnti del mouse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica non viene inviato da un controllo di visualizzazione albero con lo stile [**\_ TVS DISABLEDRAGDROP.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ BEGINDRAGW** (Unicode) e **TVN \_ BEGINDRAGA** (ANSI)<br/>               |



 

 





