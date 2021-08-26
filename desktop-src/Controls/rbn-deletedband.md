---
title: RBN_DELETEDBAND di notifica (Commctrl.h)
description: Inviato da un controllo Rebar dopo l'eliminazione di una banda. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e60d1a8ad062d77800ccc9e2790718f5d8c8dcac2fb87a37f62b8f1131e5cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985241"
---
# <a name="rbn_deletedband-notification-code"></a>Codice di notifica RBN \_ DELETEDBAND

Inviato da un controllo Rebar dopo l'eliminazione di una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) che contiene informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





