---
title: LVN_BEGINRDRAG di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che è in corso un'operazione di trascinamento della selezione che interessa il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f836e911f49464e9bba13ea09b2732e678a955ac9de01cb8bfe53e0906babff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019139"
---
# <a name="lvn_beginrdrag-notification-code"></a>Codice di notifica LVN \_ BEGINRDRAG

Notifica alla finestra padre di un controllo visualizzazione elenco che è in corso un'operazione di trascinamento della selezione che interessa il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Il **membro iItem** identifica l'elemento trascinato e gli altri membri sono zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





