---
title: TRBN_THUMBPOSCHANGING di notifica (Commctrl.h)
description: Notifica che la posizione del cursore su un trackbar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f05f67eb20c78f764957e73d2293d32e88f25a73d44d6b58f9a1c310b8d9d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751041"
---
# <a name="trbn_thumbposchanging-notification-code"></a>Codice di notifica \_ TRBN THUMBPOSCHANGING

Notifica che la posizione del cursore su un trackbar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTRBTHUMBPOSCHANGING.**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) Il chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri, inclusi i membri della struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per impedire lo spostamento del cursore nella posizione specificata.

## <a name="remarks"></a>Commenti

Inviare questa notifica ai client che non sono in ascolto di [**messaggi WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





