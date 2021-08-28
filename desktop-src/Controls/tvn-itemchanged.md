---
title: TVN_ITEMCHANGED di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che gli attributi dell'elemento sono stati modificati. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED del codice di notifica Windows controlli
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
ms.openlocfilehash: d140346d66a87bd394bc5aa36555b8accedef56891e722a4b28272e22f804ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018649"
---
# <a name="tvn_itemchanged-notification-code"></a>Codice di notifica \_ TVN ITEMCHANGED

Notifica alla finestra padre di un controllo visualizzazione albero che gli attributi dell'elemento sono stati modificati. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) che descrive l'elemento modificato. Il **membro uChanged** è impostato su TVIF \_ STATE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE** per accettare la modifica oppure **TRUE per** impedire la modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) e **TVN \_ ITEMCHANGEDA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TVN \_ ITEMCHANGING](tvn-itemchanging.md)
</dt> </dl>

 

 





