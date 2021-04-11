---
title: Codice di notifica LVN_ITEMCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è in corso la modifica di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- Controlli di Windows per il codice di notifica LVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965012"
---
# <a name="lvn_itemchanging-notification-code"></a>\_Codice di notifica ITEMCHANGING di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che è in corso la modifica di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che identifica l'elemento e specifica quali attributi sono in corso di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per impedire la modifica o **false** per consentire la modifica.

## <a name="remarks"></a>Commenti

Se il controllo elenco-visualizzazione dispone dello stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) , i \_ codici di notifica LVN ITEMCHANGING non vengono inviati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





