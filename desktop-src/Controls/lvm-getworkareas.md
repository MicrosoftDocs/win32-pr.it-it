---
title: LVM_GETWORKAREAS messaggio (Commctrl.h)
description: Recupera le aree di lavoro da un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetWorkAreas.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aed6173ef00860900d7690199cfb2c81535f088790290e30cc01898666bb068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968231"
---
# <a name="lvm_getworkareas-message"></a>Messaggio \_ LVM GETWORKAREAS

Recupera le aree di lavoro da un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di [**strutture RECT**](/previous-versions//dd162897(v=vs.85)) nella matrice in corrispondenza di *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice [**di strutture RECT**](/previous-versions//dd162897(v=vs.85)) che ricevono le aree di lavoro correnti del controllo di visualizzazione elenco. I valori in queste strutture sono in coordinate client. *wParam* specifica il numero di strutture in questa matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso List-View controlli](using-list-view-controls.md)
</dt> </dl>

 

