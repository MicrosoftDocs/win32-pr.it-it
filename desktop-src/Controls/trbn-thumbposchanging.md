---
title: Codice di notifica TRBN_THUMBPOSCHANGING (COMmctrl. h)
description: Notifica che la posizione del cursore in un controllo TrackBar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- Controlli di Windows per il codice di notifica TRBN_THUMBPOSCHANGING
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
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969157"
---
# <a name="trbn_thumbposchanging-notification-code"></a>\_Codice di notifica THUMBPOSCHANGING di Trbn

Notifica che la posizione del cursore in un controllo TrackBar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) . Il chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri, inclusi i membri della struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per impedire che il controllo Thumb venga spostato nella posizione specificata.

## <a name="remarks"></a>Commenti

Inviare questa notifica ai client che non sono in ascolto dei messaggi [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





