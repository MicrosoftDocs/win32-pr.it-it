---
title: TVN_ITEMCHANGING codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che gli attributi dell'elemento stanno per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING codice di notifica Windows controlli
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
ms.openlocfilehash: 85416e22562720455da3e3c03c95b3cee25b5f0f7420a31250b244f47dab0caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957870"
---
# <a name="tvn_itemchanging-notification-code"></a>Codice di \_ notifica TVN ITEMCHANGING

Notifica alla finestra padre di un controllo visualizzazione albero che gli attributi dell'elemento stanno per cambiare. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) che descrive l'elemento che viene modificato. Il **membro uChanged** è impostato su TVIF \_ STATE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE** per accettare la modifica oppure **TRUE per** impedire la modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) e **TVN \_ ITEMCHANGINGA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TVN \_ ITEMCHANGED](tvn-itemchanged.md)
</dt> </dl>

 

 





