---
title: TBN_DRAGOVER di notifica (Commctrl.h)
description: Verifica se deve essere inviato un messaggio MARKBUTTON da TB \_ per un pulsante trascinato. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718a51f14f096edbd8df72b0c5fc33ca65ec0c303a095f108981482c9fb3cda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829345"
---
# <a name="tbn_dragover-notification-code"></a>Codice di notifica \_ TBN DRAGOVER

Verifica se deve essere inviato un [**messaggio \_ MARKBUTTON da TB**](tb-markbutton.md) per un pulsante trascinato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) che specifica su quale elemento viene trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**FALSE se** la barra degli strumenti deve inviare un messaggio MARKBUTTON DA \_ TB; in caso **contrario, TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





