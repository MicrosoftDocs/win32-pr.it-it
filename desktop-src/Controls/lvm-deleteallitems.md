---
title: LVM_DELETEALLITEMS messaggio (Commctrl.h)
description: Rimuove tutti gli elementi da un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView DeleteAllItems.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958410"
---
# <a name="lvm_deleteallitems-message"></a>Messaggio LVM \_ DELETEALLITEMS

Rimuove tutti gli elementi da un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView DeleteAllItems.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Quando un controllo visualizzazione elenco riceve il messaggio **LVM \_ DELETEALLITEMS,** invia il codice di notifica [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) alla finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





