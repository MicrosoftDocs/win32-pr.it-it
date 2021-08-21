---
title: LVN_BEGINDRAG di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che è in corso un'operazione di trascinamento della selezione che coinvolge il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c86730f624e74420ccf8e9c3b47035ce075ac20448d9bedb99784ec1ca1c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170357"
---
# <a name="lvn_begindrag-notification-code"></a>Codice di notifica \_ LVN BEGINDRAG

Notifica alla finestra padre di un controllo visualizzazione elenco che è in corso un'operazione di trascinamento della selezione che coinvolge il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Il **membro iItem** identifica l'elemento trascinato e gli altri membri sono pari a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





