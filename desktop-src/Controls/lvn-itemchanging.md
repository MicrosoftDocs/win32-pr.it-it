---
title: LVN_ITEMCHANGING codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco la modifica di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c53eaf5ea2de3a19ea0934be8967e81d0e6d7a1728063f6b9a0a5958715cdf24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005648"
---
# <a name="lvn_itemchanging-notification-code"></a>Codice di notifica LVN \_ ITEMCHANGING

Notifica alla finestra padre di un controllo visualizzazione elenco la modifica di un elemento. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che identifica l'elemento e specifica quale dei relativi attributi viene modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per impedire la modifica oppure **FALSE** per consentire la modifica.

## <a name="remarks"></a>Commenti

Se il controllo visualizzazione elenco ha lo stile [**LVS \_ OWNERDATA,**](list-view-window-styles.md) i codici di notifica LVN \_ ITEMCHANGING non vengono inviati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





