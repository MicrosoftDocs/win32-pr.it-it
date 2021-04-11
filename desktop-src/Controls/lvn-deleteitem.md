---
title: Codice di notifica LVN_DELETEITEM (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- Controlli di Windows per il codice di notifica LVN_DELETEITEM
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121766"
---
# <a name="lvn_deleteitem-notification-code"></a>\_Codice di notifica DeleteItem di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Il membro **iItem** identifica l'elemento da eliminare. Se il controllo non ha lo stile **\_ OWNERDATA di LVS** , il *lParam* corrisponde ai dati definiti dall'applicazione associati all'elemento. Tutti gli altri membri di questa struttura sono pari a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Non aggiungere, eliminare o ridisporre gli elementi nella visualizzazione elenco durante l'elaborazione del codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





