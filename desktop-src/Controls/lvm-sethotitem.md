---
title: LVM_SETHOTITEM messaggio (Commctrl.h)
description: Imposta l'elemento a caldo per un controllo di visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetHotItem.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6937cbed8150bf14eb71e167b8ed54d6f6b47ae995a3af989613cba30c7ca3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077241"
---
# <a name="lvm_sethotitem-message"></a>Messaggio \_ LVM SETHOTITEM

Imposta l'elemento a caldo per un controllo di visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetHotItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento da impostare come elemento a caldo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento precedentemente in stato di hot.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





