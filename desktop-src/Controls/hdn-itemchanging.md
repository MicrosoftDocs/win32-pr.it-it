---
title: HDN_ITEMCHANGING di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo intestazione che gli attributi di un elemento intestazione stanno per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beeee8256be3cda1e872fb481bb344e319c80d426e747391539ae5fec9f3c6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170951"
---
# <a name="hdn_itemchanging-notification-code"></a>Codice di \_ notifica ITEMCHANGING HDN

Notifica alla finestra padre di un controllo intestazione che gli attributi di un elemento intestazione stanno per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione e sull'elemento di intestazione, inclusi gli attributi che stanno per cambiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE** per consentire le modifiche o **TRUE per** impedirle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ ITEMCHANGINGW** (Unicode) e **HDN \_ ITEMCHANGINGA** (ANSI)<br/>         |



 

 





