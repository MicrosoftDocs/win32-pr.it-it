---
title: TVN_DELETEITEM di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che è in corso l'eliminazione di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9244fd7a848adc3f2d82f48177482c0ffb8cbe1484bc501accfb7ffab3aefbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408247"
---
# <a name="tvn_deleteitem-notification-code"></a>Codice di notifica \_ TVN DELETEITEM

Notifica alla finestra padre di un controllo visualizzazione albero che è in corso l'eliminazione di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Il **membro itemOld** è una [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **hItem** e **lParam** contengono informazioni valide sull'elemento da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Se il **membro lParam** della struttura TVITEM punta alla memoria allocata dall'applicazione, è possibile liberarla quando si riceve il codice di notifica [**TVN**](/windows/win32/api/commctrl/ns-commctrl-tvitema) \_ DELETEITEM.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ DELETEITEMW** (Unicode) e **TVN \_ DELETEITEMA** (ANSI)<br/>             |



 

 





